---
UID: NF:clusapi.BackupClusterDatabase
title: BackupClusterDatabase function
author: windows-sdk-content
description: Creates a backup of the cluster database and all registry checkpoints.
old-location: mscs\backupclusterdatabase.htm
tech.root: mscs
ms.assetid: c381b7d3-cc60-45cf-a7f0-eebf44557bcf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: BackupClusterDatabase, BackupClusterDatabase function [Failover Cluster], _wolf_backupclusterdatabase, clusapi/BackupClusterDatabase, mscs.backupclusterdatabase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - BackupClusterDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BackupClusterDatabase function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this function was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Creates a backup of the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and 
    all registry <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">checkpoints</a>.


## -parameters




### -param hCluster [in]

Handle to the cluster to be backed up.


### -param lpszPathName [in]

Null-terminated Unicode string specifying the path to where the backup should be created. Cluster 
      configuration information will be saved to this location; this is sensitive data that should be protected. For 
      example, this data can be protected by using an access control list to restrict access to the location where the 
      data is stored.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



Ideally, the specified path should be a path visible to all cluster 
     <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>, such as a UNC path. At minimum, the path must be visible to 
     the node that currently owns the <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>. Do not 
     include a filename in the path or the function will fail, returning <b>ERROR_DIRECTORY</b>. 
     The path can include a trailing backslash.

One way to ensure that an appropriate path exists is to create a temporary network share, as follows:

<ul>
<li>Call the function <a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a> to create a temporary 
      network share. All cluster nodes must have write access to this share.</li>
<li>Call <b>BackupClusterDatabase</b>, specifying 
      the temporary share in the <i>lpszPathName</i> parameter.</li>
<li>Copy the backup files (see below) to one or more safe storage locations.</li>
<li>Call the function <a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a> to delete the 
      share.</li>
</ul>
The backup contains the following files.

<table>
<tr>
<th>Path\File</th>
<th>Description</th>
</tr>
<tr>
<td>
<i>lpszPathName</i>\chk????.tmp

</td>
<td>
Snapshot files.

</td>
</tr>
<tr>
<td>
<i>lpszPathName</i>\quolog.log

</td>
<td>
The quorum log file.

</td>
</tr>
<tr>
<td>
<i>lpszPathName</i>\&lt;GUID of resource&gt;\*.CPT

</td>
<td>
The registry checkpoint files for the resource identified by GUID.

</td>
</tr>
<tr>
<td>
<i>lpszPathName</i>\&lt;GUID of resource&gt;\*.CPR

</td>
<td>
The crypto checkpoint files for the resource identified by GUID.

</td>
</tr>
<tr>
<td>
<i>lpszPathName</i>\Clusbackup.dat

</td>
<td>
Backup completion marker file (read-only, hidden, 0-byte file)

</td>
</tr>
</table>
 

Subsequent <b>BackupClusterDatabase</b> operations 
     that use the same <i>lpszPath</i> parameter will overwrite the existing backup files.

If possible, make multiple copies of the backup directory on different media and store these copies in separate 
     locations.


#### Examples

The following example illustrates a static backup routine. For a more complete example 
     incorporating <a href="https://msdn.microsoft.com/a0524363-c5dc-449a-aaf6-9bcd9522c9eb">RestoreClusterDatabase</a>, see 
     <a href="https://msdn.microsoft.com/a8914274-7cbc-4f10-9611-f625994f14c8">Backing Up and Restoring the Cluster Configuration</a>. 
     This example uses the <a href="https://msdn.microsoft.com/fc2032d2-40a5-45bd-8661-1e778789bad6">ClusDocEx.h</a> header file defined in the 
     Failover Cluster documentation.


```cpp

int main( void )
 {
  HCLUSTER hCluster     = NULL;
  WCHAR szClusterName[] = L"CLUSTER_NAME";
  WCHAR szPath[]        = L"\\\\ClusBack\\19991215";
  DWORD dwResult        = ERROR_SUCCESS;
 
  if( ( hCluster = OpenCluster( szClusterName ) ) != NULL )
   {
    dwResult = BackupClusterDatabase( hCluster, szPath );
    CloseCluster( hCluster );
   }
  else
    dwResult = GetLastError();

  if( dwResult == ERROR_SUCCESS )
   {
    wprintf( L"\nDone. The cluster database has been backed up to %s. ", szPath );
    wprintf( L"The backup consists of the following files:\n    chk????.tmp\n"
             L"    quolog.log\n    *.cpt\n    *.cpr\n\n" );
    return 0;
   }
  else
   {
    wprintf( L"The operation failed (%d)\n", dwResult );
    return 1;
   }
 }

```





## -see-also




<a href="https://msdn.microsoft.com/0f492e51-f364-40f1-b2c8-478f707f079d">Backup and Restore Functions</a>



<a href="https://msdn.microsoft.com/a0524363-c5dc-449a-aaf6-9bcd9522c9eb">RestoreClusterDatabase</a>
 

 

