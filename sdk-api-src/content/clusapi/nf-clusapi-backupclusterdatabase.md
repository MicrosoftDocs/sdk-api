---
UID: NF:clusapi.BackupClusterDatabase
title: BackupClusterDatabase function (clusapi.h)
description: Creates a backup of the cluster database and all registry checkpoints.
helpviewer_keywords: ["BackupClusterDatabase","BackupClusterDatabase function [Failover Cluster]","_wolf_backupclusterdatabase","clusapi/BackupClusterDatabase","mscs.backupclusterdatabase"]
old-location: mscs\backupclusterdatabase.htm
tech.root: MsCS
ms.assetid: c381b7d3-cc60-45cf-a7f0-eebf44557bcf
ms.date: 12/05/2018
ms.keywords: BackupClusterDatabase, BackupClusterDatabase function [Failover Cluster], _wolf_backupclusterdatabase, clusapi/BackupClusterDatabase, mscs.backupclusterdatabase
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BackupClusterDatabase
 - clusapi/BackupClusterDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - BackupClusterDatabase
---

# BackupClusterDatabase function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this function was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Creates a backup of the <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> and 
    all registry <a href="/previous-versions/windows/desktop/mscs/checkpointing">checkpoints</a>.

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
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

Ideally, the specified path should be a path visible to all cluster 
     <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a>, such as a UNC path. At minimum, the path must be visible to 
     the node that currently owns the <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>. Do not 
     include a filename in the path or the function will fail, returning <b>ERROR_DIRECTORY</b>. 
     The path can include a trailing backslash.

One way to ensure that an appropriate path exists is to create a temporary network share, as follows:

<ul>
<li>Call the function <a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a> to create a temporary 
      network share. All cluster nodes must have write access to this share.</li>
<li>Call <b>BackupClusterDatabase</b>, specifying 
      the temporary share in the <i>lpszPathName</i> parameter.</li>
<li>Copy the backup files (see below) to one or more safe storage locations.</li>
<li>Call the function <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedel">NetShareDel</a> to delete the 
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
     incorporating <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-restoreclusterdatabase">RestoreClusterDatabase</a>, see 
     <a href="/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-cluster-configuration">Backing Up and Restoring the Cluster Configuration</a>. 
     This example uses the <a href="/previous-versions/windows/desktop/mscs/clusdocex-h">ClusDocEx.h</a> header file defined in the 
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

<a href="/previous-versions/windows/desktop/mscs/backup-and-restore-functions">Backup and Restore Functions</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-restoreclusterdatabase">RestoreClusterDatabase</a>