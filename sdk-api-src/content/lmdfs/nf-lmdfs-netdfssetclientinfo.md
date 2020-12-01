---
UID: NF:lmdfs.NetDfsSetClientInfo
title: NetDfsSetClientInfo function (lmdfs.h)
description: Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.
helpviewer_keywords: ["101","102","NetDfsSetClientInfo","NetDfsSetClientInfo function [Distributed File System]","_win32_netdfssetclientinfo","dfs.netdfssetclientinfo","fs.netdfssetclientinfo","lmdfs/NetDfsSetClientInfo","netmgmt.netdfssetclientinfo"]
old-location: dfs\netdfssetclientinfo.htm
tech.root: Dfs
ms.assetid: 4c95dffb-a092-45ad-9a3f-37d3abbf4427
ms.date: 12/05/2018
ms.keywords: 101, 102, NetDfsSetClientInfo, NetDfsSetClientInfo function [Distributed File System], _win32_netdfssetclientinfo, dfs.netdfssetclientinfo, fs.netdfssetclientinfo, lmdfs/NetDfsSetClientInfo, netmgmt.netdfssetclientinfo
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
 - NetDfsSetClientInfo
 - lmdfs/NetDfsSetClientInfo
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
 - NetDfsSetClientInfo
---

# NetDfsSetClientInfo function


## -description

Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.

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

Pointer to a string that specifies the DFS link target server name. This parameter is optional. For more information, see the Remarks section.

### -param ShareName [in, optional]

Pointer to a string that specifies the DFS link target share name. This parameter is optional. For additional information, see the following Remarks section.

### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 101

Set the local DFS link's storage status. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101">DFS_INFO_101</a> structure.



#### 102

Set the local DFS link time-out. The <i>Buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102">DFS_INFO_102</a> structure. For more information, see the following Remarks section.

### -param Buffer [in]

Pointer to a buffer that contains the information to be set. The format of this information depends on the value of the <i>Level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller must have Administrator privilege on the DFS server. For more information about calling functions that require administrator privileges, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Setting the time-out to zero may not immediately delete the local cached copy of the DFS link, because threads may be referencing the entry.

Because there is only one time-out on a DFS link, the <i>ServerName</i> and <i>ShareName</i> parameters are ignored for level 102.

The <b>DFS_STORAGE_STATE_ONLINE</b> and <b>DFS_STORAGE_STATE_OFFLINE</b> bits will be ignored. The <b>DFS_STORAGE_STATE_ACTIVE</b> bit is valid only if no files are open to the active computer.

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101">DFS_INFO_101</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102">DFS_INFO_102</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>