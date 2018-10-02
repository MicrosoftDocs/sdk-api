---
UID: NF:clusapi.RestoreClusterDatabase
title: RestoreClusterDatabase function
author: windows-sdk-content
description: Restores the cluster database and restarts the Cluster service on the node from which the function is called. This node is called the restoring node.
old-location: mscs\restoreclusterdatabase.htm
tech.root: MsCS
ms.assetid: a0524363-c5dc-449a-aaf6-9bcd9522c9eb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RestoreClusterDatabase, RestoreClusterDatabase function [Failover Cluster], _wolf_restoreclusterdatabase, clusapi/RestoreClusterDatabase, mscs.restoreclusterdatabase
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
 - RestoreClusterDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RestoreClusterDatabase function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this function was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Restores 
    the <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> and restarts the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> on the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> from which the function is called. This node is called the 
    restoring node.


## -parameters




### -param lpszPathName [in]

Null-terminated Unicode string specifying the path to the backup file. Cluster configuration information is 
       contained in this location; this is sensitive data that should be protected. For example, this data can be 
       protected by using an access control list to restrict access to the location where the data is stored.


### -param bForce [in]

If <b>FALSE</b>, the restore operation will not be completed if either of the following 
       circumstances applies:

<ul>
<li>Other nodes are currently active.</li>
<li>The partition layout of the current quorum resource is not identical to the partition layout of the 
        quorum resource that was in place when the backup was made. (The term "partition layout" 
        refers to the number of partitions on the disk and the offsets to each partition. The disk signature and drive 
        letter assignments do not have to be identical.)</li>
</ul>
Setting <i>bForce</i> to <b>TRUE</b> causes the operation to proceed 
       regardless of these preceding circumstances; however, the operation may still fail for other reasons.


### -param lpszQuorumDriveLetter [in, optional]

Optional. Identifies the drive letter of the quorum resource on which the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> will be restored. Use this 
       parameter only if the quorum resource has been replaced since the backup was made. The string must be formatted 
       as follows:

<ul>
<li>The first character must be alphabetic, that is, in the range 'a'-'z' or 'A'-'Z'.</li>
<li>The second character must be a colon (':').</li>
<li>The third character must be a terminating null ('\0').</li>
</ul>

## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following are possible error 
       codes.




## -remarks



If the restore operation is successful, the restoring node forms a 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> according to the configuration data in the 
     restored cluster database. As other nodes join the cluster, they update their cluster databases from the database 
     on the restoring node.

Note that <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster disks</a> other than the quorum 
     resource that have added or changed since the backup was made will not be recognized by the restored cluster 
     database and will remain <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">offline</a> even if the restore 
     operation is successful. New <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> must be created for these 
     disks (see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369328(v=VS.85).aspx">Creating a Physical Disk Resource</a>).

The following general procedure is recommended for any cluster restore routine:

<ol>
<li>Call <b>RestoreClusterDatabase</b> with 
      <i>bForce</i> set to <b>FALSE</b> and no drive letter specified. This is 
      the best approach because, if successful, the operation does not have to force configuration changes.</li>
<li>
If the first call fails, let the user decide whether to force the procedure to continue or manually fix the 
      problem. Be sure to communicate the implications of each decision.

<table>
<tr>
<th>Return value</th>
<th>Action if forced</th>
<th>Manual fix</th>
</tr>
<tr>
<td>
<b>ERROR_CLUSTER_NODE_UP</b>

</td>
<td>
The restore operation will stop the Cluster service on all other nodes.

</td>
<td>
User manually shuts down the Cluster service on all other cluster nodes. The command 
          <b>Net Stop ClusSvc</b> is sufficient; a complete power-down is unnecessary.

</td>
</tr>
<tr>
<td>
<b>ERROR_QUORUM_DISK_NOT_FOUND</b>

</td>
<td>
User must supply the drive letter of the quorum resource. The restore operation will change the disk's 
          signature and drive letter to the values stored in the backup.

</td>
<td>
User repartitions the quorum disk so that the layout is identical to the layout stored in the backup.

</td>
</tr>
</table>
 

If the user agrees to force continuation, call 
       <b>RestoreClusterDatabase</b> with 
       <i>bForce</i> set to <b>TRUE</b> and the drive letter specified (if 
       applicable). Forcing does not guarantee success. If the restore operation fails again, test the return value 
       and respond appropriately.

</li>
</ol>

#### Examples

The following example illustrates the procedure described above. For a more complete example that includes 
     <a href="https://msdn.microsoft.com/en-us/library/Aa367185(v=VS.85).aspx">BackupClusterDatabase</a>, see the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa367184(v=VS.85).aspx">Backing Up and Restoring the Cluster Configuration</a>. 
     This example uses the  <a href="https://msdn.microsoft.com/en-us/library/Aa367743(v=VS.85).aspx">ClusDocEx.h</a> header file defined in the 
     Failover Cluster documentation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
int main( void )
{
    WCHAR szPath[] = L"c:\\ClusBack\\19991215";
    WCHAR szInput[3];
    BOOL bForce = FALSE;
    DWORD dwResult = ERROR_SUCCESS;

    // First try: no force
    dwResult = RestoreClusterDatabase( szPath, FALSE, NULL );
    
    // Allow user to force shutdown if necessary.
    if( dwResult == ERROR_CLUSTER_NODE_UP )
    {
        wprintf( L"The operation failed because other cluster nodes are currently active. " );
        wprintf( L"The Cluster service must be shut down on all other nodes in order for this operation to succeed." );
        wprintf( L"Enter 'f' to force automatic shutdown, or any other key to exit for manual shutdown:  " );
        fgetws( szInput, 2, stdin );
        if( towupper( szInput[0] ) == L'F' )
            dwResult = RestoreClusterDatabase( szPath, TRUE, NULL );
    }

    // Allow user to locate quorum resource if necessary.
    if( dwResult == ERROR_QUORUM_DISK_NOT_FOUND )
    {
        wprintf( L"\n\nERROR: QUORUM DISK NOT FOUND\n" );
        wprintf( L"The restore routine cannot find a quorum resource with the same partition layout as the quorum resource described in the backup. " );
        wprintf( L"The existing quorum resource must have a layout (number of partitions and offsets to each partition) identical to the layout stored in the backup.\n" );
        wprintf( L"Enter the drive letter of the quorum resource to force continuation, or any non-letter key to exit:  " );
        fgetws( szInput, 3, stdin );
        if( iswalpha( szInput[0] ) )
        {
            szInput[1] = L':';
            szInput[2] = L'\0';
            dwResult = RestoreClusterDatabase( szPath, TRUE, szInput );
        }
    }

    // Only one force attempt per error, then report success or failure. 
    if( dwResult == ERROR_SUCCESS )
    {
        wprintf( L"\n\nSUCCESS\n" );
        wprintf( L"The restore routine succeeded. Start the Cluster service on the other cluster nodes to complete the restore operation." );
        wprintf( L"As nodes join the cluster, they will update their cluster databases to match the restored configuration." ); 
        return 0;
    }
    else
    {
        wprintf( L"RestoreClusterDatabase failed (%d)\n", dwResult );
        return 1;
    }

}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa367185(v=VS.85).aspx">BackupClusterDatabase</a>
 

 

