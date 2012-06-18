# Magento Debug Toolbar 
Based on robhudson's awesome work (<https://github.com/robhudson/django-debug-toolbar>) we've created a debug toolbar for Magento.
It is installed as a Magento module without hacking Magento's core.

Basic features are implemented and few others will come soon. Check the screenshots for current features: <https://github.com/madalinoprea/magneto-debug/wiki>

Or demo video on YouTube: http://www.youtube.com/watch?v=aqvgrmebcu4

## FEATURES 
 - Now available in Admin (1.0.1 RC - fancy for I'm laizy to create Magento Connect package)
 - Magento module listing; Toggle Magento modules on the fly
 - Search configuration keys
 - Display peak memory usage, script execution time
 - Request information (controller name, action name, cookies variables, session variables, GET and POST variables)
 - Models instantiated
 - SQL queries executed for current request; ability to see queries' result or queries' execution plan (EXPLAIN)
 - List Magento configuration
 - Print layout handles for current request
 - Find xml files where a specific layout handle is defined
 - Created blocks, their associated templates; Preview templates' source code
 - Quick actions: 
    - Toggle template hints
    - Clear cache
    - Toggle inline translation

## KNOWN ISSUES
We're working to correct these:

 - To enable SQL profiler manually you have to add in your local.xml profiler tag `<profiler>1</profiler>` under connection, like in the example below:
<pre><code>
    <default_setup>
        <connection>
            <host><![CDATA[/var/run/mysqld/mysqld.sock]]></host>
            <username><![CDATA[root]]></username>
            <password><![CDATA[]]></password>
            <dbname><![CDATA[magento]]></dbname>
            <active>1</active>
            <profiler>1</profiler>
        </connection>
    </default_setup>
</code></pre>

 - `Disable SQL Profiler` is not working, but `Enable SQL Profiler` works like a charm (or not)
