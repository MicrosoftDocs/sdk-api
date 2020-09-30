---
UID: NF:lmdfs.NetDfsGetClientInfo
title: NetDfsGetClientInfo function (lmdfs.h)
description: Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.
helpviewer_keywords: ["1","2","3","4","NetDfsGetClientInfo","NetDfsGetClientInfo function [Distributed File System]","_win32_netdfsgetclientinfo","dfs.netdfsgetclientinfo","fs.netdfsgetclientinfo","lmdfs/NetDfsGetClientInfo"]
old-location: dfs\netdfsgetclientinfo.htm
tech.root: Dfs
ms.assetid: 065ec002-cb90-4d78-a70c-6ac37f71994f
ms.date: 12/05/2018
ms.keywords: 1, 2, 3, 4, NetDfsGetClientInfo, NetDfsGetClientInfo function [Distributed File System], _win32_netdfsgetclientinfo, dfs.netdfsgetclientinfo, fs.netdfsgetclientinfo, lmdfs/NetDfsGetClientInfo
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
 - NetDfsGetClientInfo
 - lmdfs/NetDfsGetClientInfo
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
 - NetDfsGetClientInfo
---

# NetDfsGetClientInfo function


## -description

Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.

## -parameters

### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace; <i>DomDfsname</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

or

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>

where the values of the names are the same as those described previously.

This parameter is required.

### -param ServerName [in, optional]

Pointer to a string that specifies the name of the DFS root target or link target server. This parameter is optional.

### -param ShareName [in, optional]

Pointer to a string that specifies the name of the share corresponding to the DFS root target or link target. This parameter is optional.

### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 1

Return the DFS root  or DFS link name. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and target information. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, <b>GUID</b>, time-out, and target information. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a> structure.

### -param Buffer [out]

Pointer to the address of a buffer that receives the requested information. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required for using the 
<b>NetDfsGetClientInfo</b> function.

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo">NetDfsSetClientInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>