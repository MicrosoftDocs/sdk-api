---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RestoreClusterDatabase function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this function was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Restores 
    the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and restarts the 
    <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> on the 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from which the function is called. This node is called the 
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
       <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> will be restored. Use this 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
       codes.




## -remarks



If the restore operation is successful, the restoring node forms a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> according to the configuration data in the 
     restored cluster database. As other nodes join the cluster, they update their cluster databases from the database 
     on the restoring node.

Note that <a href="c_gly.htm">cluster disks</a> other than the quorum 
     resource that have added or changed since the backup was made will not be recognized by the restored cluster 
     database and will remain <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">offline</a> even if the restore 
     operation is successful. New <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> must be created for these 
     disks (see 
    <a href="https://msdn.microsoft.com/003bc879-d526-4f7d-8f58-a9002f78819d">Creating a Physical Disk Resource</a>).

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
     <a href="https://msdn.microsoft.com/c381b7d3-cc60-45cf-a7f0-eebf44557bcf">BackupClusterDatabase</a>, see the 
     <a href="https://msdn.microsoft.com/a8914274-7cbc-4f10-9611-f625994f14c8">Backing Up and Restoring the Cluster Configuration</a>. 
     This example uses the  <a href="https://msdn.microsoft.com/fc2032d2-40a5-45bd-8661-1e778789bad6">ClusDocEx.h</a> header file defined in the 
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




<a href="https://msdn.microsoft.com/c381b7d3-cc60-45cf-a7f0-eebf44557bcf">BackupClusterDatabase</a>
 

 

