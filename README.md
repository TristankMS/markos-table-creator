# markos-table-creator
It's all Marko

# Usage

```Powershell
.\tablecreator.ps1 -FullResourceId /subscriptions/12345678-1234-1234-1234-123456789abc/resourcegroups/rg-name/providers/microsoft.operationalinsights/workspaces/sentinel-name`
 -tableName CommonSecurityLog -newTableName CommonSecurityLog_lakey_CL -plan Auxiliary -retention 30 -totalretention 180
```


# Background

Marko Lauren created the very helpful [table creator script](https://github.com/markolauren/sentinel/tree/main/tableCreator%20tool), but I need to flit between environments, and I don't like actually editing scripts when I don't have to, so I added the new -FullResourceId parameter (semi-poached from the Sentinel SOA Collector).

Useful for scenarios where you want to send a log directly to a low-cost tier, say ([Auxiliary or Sentinel data lake](https://tristank.substack.com/p/shove-syslog-and-cef-into-data-lake)).

# More background

And I couldn't download the forked repo on my Windows based dev system... I assume due to the presence of a file aux.conf ? (COM1 Aux Con LPT still issues I wonder?)

And I couldn't delete the file from GitHub either, super-interestingly..

So! Added support for -FullResourceID.

I'll send it upstream.

