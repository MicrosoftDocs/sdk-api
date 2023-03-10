---
UID: NF:lmdfs.NetDfsEnum
title: NetDfsEnum function (lmdfs.h)
description: Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.
helpviewer_keywords: ["1","2","200","3","300","4","5","6","8","9","NetDfsEnum","NetDfsEnum function [Distributed File System]","_win32_netdfsenum","dfs.netdfsenum","fs.netdfsenum","lmdfs/NetDfsEnum","netmgmt.netdfsenum"]
old-location: dfs\netdfsenum.htm
tech.root: Dfs
ms.assetid: c05a8d78-41f4-4c19-a25e-ef4885869584
ms.date: 12/05/2018
ms.keywords: 1, 2, 200, 3, 300, 4, 5, 6, 8, 9, NetDfsEnum, NetDfsEnum function [Distributed File System], _win32_netdfsenum, dfs.netdfsenum, fs.netdfsenum, lmdfs/NetDfsEnum, netmgmt.netdfsenum
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
 - NetDfsEnum
 - lmdfs/NetDfsEnum
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
 - NetDfsEnum
---

# NetDfsEnum function


## -description

Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by 
    a server.

## -parameters

### -param DfsName [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of the DFS root or link.

When you specify information level 200 
       (<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200">DFS_INFO_200</a>), this parameter is the name of a 
       domain. When you specify information level 300 
       (<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300">DFS_INFO_300</a>), this parameter is the name of a 
       server.

For all other levels, the string can be in one of the following four forms:

<i>ServerName</i>&#92;<i>DfsName</i>

or

<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>Dfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The string can also be of the following forms:

<i>DomainName</i>&#92;<i>DomainName\DomDfsName</i>

or

<i>DomainName</i>&#92;<i>DomDfsName</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS root; 
       <i>DomDfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

You can precede the string with backslashes (\\), but they are not required. This parameter is required.

### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 1

Return the name of the DFS root and all links under the root. The <i>Buffer</i> 
        parameter points to an array of <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a> 
        structures.



#### 2

Return the name, comment, status, and the number of targets for the DFS root and all links under the 
        root. The <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a> structures.



#### 3

Return the name, comment, status, number of targets, and information about each target for the DFS root 
        and all links under the root. The <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a> structures.



#### 4

Return the name, comment, status, <b>GUID</b>, time-out, number of targets, and information about each target 
        for the DFS root and all links under the root. The <i>Buffer</i> parameter points to an 
        array of <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a> structures.



#### 5

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, and number of targets for a DFS 
        root and all links under the root. The <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5">DFS_INFO_5</a> structures.



#### 6

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information for a root 
        or link, and a list of DFS targets. The <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a> structures.



#### 8

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, number of targets, and link 
        reparse point security descriptors for a DFS root and all links under the root. The 
        <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8">DFS_INFO_8</a> structures.



#### 9

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information, link 
        reparse point security descriptors, and a list of DFS targets for a root or link. The 
        <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9">DFS_INFO_9</a> structures.



#### 200

Return the list of domain-based DFS namespaces in the domain. The <i>Buffer</i> 
        parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200">DFS_INFO_200</a> structures.



#### 300

Return the stand-alone and domain-based DFS namespaces hosted by a server. The 
        <i>Buffer</i> parameter points to an array of 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300">DFS_INFO_300</a> structures.

### -param PrefMaxLen [in]

Specifies the number of bytes that should be returned by this function in the information structure buffer. 
      If this parameter is <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. 
      For more information, see the following Remarks section. This parameter is ignored if you specify level 200 or 
      level 300.

### -param Buffer [out]

Pointer to a buffer that receives the requested information structures. The format of this data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

### -param EntriesRead [out]

Pointer to a value that receives the actual number of entries returned in the response.

### -param ResumeHandle [in, out]

Pointer to a value that contains a handle to be used for continuing an enumeration when more data is available than can be returned in a single call to this function. The handle should be zero on the first call and left unchanged for subsequent calls.  For more information, see the following Remarks section.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If no more entries are available to be enumerated, the return value is <b>ERROR_NO_MORE_ITEMS</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required for using the 
<b>NetDfsEnum</b> function.

Call the 
<b>NetDfsEnum</b> function with the <i>ResumeHandle</i> parameter set to zero to begin the enumeration. To continue the enumeration operation, call this function with the <i>ResumeHandle</i> returned by the previous call to 
<b>NetDfsEnum</b>. If this function does not return <b>ERROR_NO_MORE_ITEMS</b>, subsequent calls to this API will return the remaining links. Once <b>ERROR_NO_MORE_ITEMS</b> is returned, all available DFS links have been retrieved.

The 
<b>NetDfsEnum</b> function allocates the memory required for the information structure buffer. If you specify an amount in the <i>PrefMaxLen</i> parameter, it restricts the memory that the function returns. However, the actual size of the memory that the 
<b>NetDfsEnum</b> function allocates can be greater than the amount you specify. For additional information see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

Due to the possibility of concurrent updates to the DFS namespace, the caller should not assume completeness or uniqueness of the results returned when resuming an enumeration operation.


#### Examples

The following code sample demonstrates how to list the DFS links in a named DFS root with a call to the 
<b>NetDfsEnum</b> function. The sample calls 
<b>NetDfsEnum</b>, specifying information level 3 (
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>). The sample code loops through the entries and prints the retrieved data and the status of each host server referenced by the DFS link. Finally, the sample frees the memory allocated for the information buffer.


```cpp
#include <windows.h>
#include <lm.h>
#include <lmdfs.h>
#include <stdio.h>

#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[ ])
{
    PDFS_INFO_3 pData, p;
    PDFS_STORAGE_INFO ps;
    DWORD er = 0, hResume = 0, res, i, j;

    if(argc < 2)
        wprintf(L"Syntax: %s \\\\DfsName\n", argv[0]);
    else
    {
        //
        // Call the NetDfsEnum function, specifying level 3.
        //
        res = NetDfsEnum(argv[1], 3, MAX_PREFERRED_LENGTH, (LPBYTE *) &pData, &er, &hResume);

        // Call NetDfsEnum until all available entries are returned.
        // NetDfsEnum will return ERROR_NO_MORE_ITEMS when all entries 
        // have been obtained.
        while (res == ERROR_SUCCESS)
        {
            p = pData;
            //
            // Loop through the entries; print the data.
            //
            for(i = 1; i <= er; i++)
            {
                printf("%-30S%u\n", p->EntryPath, p->NumberOfStorages);
                ps = p->Storage;
                //
                // Loop through each target.
                //
                for(j = 1; j <= p->NumberOfStorages; j++)
                {
                    //
                    // Print the status (Offline/Online) and the name 
                    // of each target referenced by the DFS link.
                    //
                    printf("    %S  ", (ps->State == DFS_STORAGE_STATE_OFFLINE) ? TEXT("Offline"):TEXT("Online "));
                    printf("\\\\%S\\%S\n", ps->ServerName, ps->ShareName);
                    ps++;
                }
                p++;
            }
            // Free the allocated buffer.
            //
            NetApiBufferFree(pData);


            res = NetDfsEnum(argv[1], 3, MAX_PREFERRED_LENGTH, (LPBYTE *) &pData, &er, &hResume);
        }


        if (res == ERROR_NO_MORE_ITEMS)
        {
            // the last of the entries have been processed.
            res = ERROR_SUCCESS;
            printf("Enumeration done\n");
        } 
        else 
        {
            // an error occurred.
            printf("Error: %u\n", res);
        }
    }
    return;
}

```

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200">DFS_INFO_200</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300">DFS_INFO_300</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5">DFS_INFO_5</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd">NetDfsAdd</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove">NetDfsRemove</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>