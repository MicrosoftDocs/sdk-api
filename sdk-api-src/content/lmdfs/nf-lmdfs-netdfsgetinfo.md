---
UID: NF:lmdfs.NetDfsGetInfo
title: NetDfsGetInfo function (lmdfs.h)
description: Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.
helpviewer_keywords: ["1","100","150","2","3","4","5","50","6","7","8","9","NetDfsGetInfo","NetDfsGetInfo function [Distributed File System]","_win32_netdfsgetinfo","dfs.netdfsgetinfo","fs.netdfsgetinfo","lmdfs/NetDfsGetInfo","netmgmt.netdfsgetinfo"]
old-location: dfs\netdfsgetinfo.htm
tech.root: Dfs
ms.assetid: bbb2f24d-1c49-4016-a16b-60fde4a78193
ms.date: 12/05/2018
ms.keywords: 1, 100, 150, 2, 3, 4, 5, 50, 6, 7, 8, 9, NetDfsGetInfo, NetDfsGetInfo function [Distributed File System], _win32_netdfsgetinfo, dfs.netdfsgetinfo, fs.netdfsgetinfo, lmdfs/NetDfsGetInfo, netmgmt.netdfsgetinfo
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetDfsGetInfo
 - lmdfs/NetDfsGetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsGetInfo
---

# NetDfsGetInfo function


## -description

Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.

## -parameters

### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

or

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>

where the values of the names are the same as those described previously.

This parameter is required.

### -param ServerName [in, optional]

This parameter is currently ignored and should be <b>NULL</b>.

### -param ShareName [in, optional]

This parameter is currently ignored and should be <b>NULL</b>.

### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 1

Return the DFS root or DFS link name. The <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. The 
        <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and  target information. The 
        <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, GUID, time-out, and target information. The 
        <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a> structure.



#### 5

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, and number of targets for a DFS 
         root and all links under the root. The <i>Buffer</i> parameter points to an array of 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5">DFS_INFO_5</a> structures.



#### 6

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information for a root 
         or link, and a list of DFS targets. The <i>Buffer</i> parameter points to an array of 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a> structures.



#### 7

Return the version number <b>GUID</b> of the DFS metadata. The <i>Buffer</i> parameter points 
         to an array of <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7">DFS_INFO_7</a> structures.



#### 8

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, number of targets, and link reparse 
         point security descriptors for a DFS root and all links under the root. The <i>Buffer</i> 
         parameter points to an array of <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8">DFS_INFO_8</a> structures.



#### 9

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information, link 
         reparse point security descriptors, and a list of DFS targets for a root or link. The 
         <i>Buffer</i> parameter points to an array of 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9">DFS_INFO_9</a> structures.



#### 50

Return the DFS metadata version and capabilities of an existing DFS namespace. The 
         <i>Buffer</i> parameter points to a 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50">DFS_INFO_50</a> structure.



#### 100

Return a comment about the DFS root or DFS link. The <i>Buffer</i> parameter points to 
        a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100">DFS_INFO_100</a> structure.



#### 150

Return the security descriptor for the DFS link's reparse point. The <i>Buffer</i> 
         parameter points to a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150">DFS_INFO_150</a> structure.

<div class="alert"><b>Note</b>  This value is natively supported only if the DFS link resides on a server that is running 
         Windows Server 2008 or later.</div>
<div> </div>

### -param Buffer [out]

Pointer to the address of a buffer that receives the requested information structures. The format of this 
      data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the 
      system and must be freed using the 
      <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, 
      see 
      <a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> 
      and 
      <a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required for using the 
    <b>NetDfsGetInfo</b> function.

An application calling the <b>NetDfsGetInfo</b> function may 
    indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of 
    the related namespace metadata from the PDC emulator master for that domain. This full synchronization could 
    happen even when root scalability mode is configured for that namespace. In order to avoid this side-effect, if 
    the intent is to only retrieve the physical UNC pathname used by a specific DFSN client machine corresponding a 
    given DFS namespace path, then one alternative is to use the WDK API 
    <a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-ntqueryinformationfile">ZwQueryInformationFile</a>, passing 
    <b>FileNetworkPhysicalNameInformation</b> as the 
    <i>FileInformationClass</i> parameter and passing the address of a caller-allocated 
    <a href="/windows-hardware/drivers/ddi/content/ntifs/ns-ntifs-_file_network_physical_name_information">FILE_NETWORK_PHYSICAL_NAME_INFORMATION</a> 
    structure as the <i>FileInformation</i> parameter. Please see the WDK for more information on 
    calling WDK APIs.


#### Examples

The following code sample demonstrates how to retrieve information about a DFS link using a call to the 
     <b>NetDfsGetInfo</b> function. The sample calls 
     <b>NetDfsGetInfo</b>, specifying information level 3 
     (<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>). If the call succeeds, the 
     sample prints information about the DFS link, including the name and status of each target referenced by the 
     link. Finally, the code sample frees the memory allocated for the information buffer.


```cpp
#include <windows.h>
#include <lm.h>
#include <lmdfs.h>
#include <stdio.h>
#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[ ])
{
   PDFS_INFO_3 pData;
   PDFS_STORAGE_INFO ps;
   DWORD er = 0, tr = 0, res, j;

   //
   // Check command line arguments.
   //
   if (argc<2)
      wprintf(L"Syntax: %s DfsEntryPath\n", argv[0]);
   else
   {
      //
      // Call the NetDfsGetInfo function, specifying level 3.
      //
      res = NetDfsGetInfo(argv[1], NULL, NULL, 3, (LPBYTE *) &pData);
      //
      // If the call succeeds, print the data.
      //
      if(res==0)
      {
         printf("%-30S Storages: %u\nComment: %S\n", pData->EntryPath, pData->NumberOfStorages, pData->Comment);
         ps = pData->Storage;
         //
         // Loop through each target.
         //
         for(j = 1; j <= pData->NumberOfStorages;j++)
         {
            //
            // Print the status (Offline/Online) and the name 
            // of each target referenced by the DFS link.
            //
            printf("    %S  ", (ps->State == DFS_STORAGE_STATE_OFFLINE) ? TEXT("Offline"): TEXT("Online "));
            printf("\\\\%S\\%S\n", ps->ServerName, ps->ShareName);
            ps++;
         }
         //
         // Free the allocated memory.
         //
         NetApiBufferFree(pData);
      }
      else
         printf("Error: %u\n", res);
   }
   return;
}

```

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100">DFS_INFO_100</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5">DFS_INFO_5</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7">DFS_INFO_7</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>