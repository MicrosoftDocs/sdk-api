---
UID: NF:lmdfs.NetDfsSetClientInfo
title: NetDfsSetClientInfo function (lmdfs.h)
author: windows-sdk-content
description: Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.
old-location: dfs\netdfssetclientinfo.htm
tech.root: Dfs
ms.assetid: 4c95dffb-a092-45ad-9a3f-37d3abbf4427
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 101, 102, NetDfsSetClientInfo, NetDfsSetClientInfo function [Distributed File System], _win32_netdfssetclientinfo, dfs.netdfssetclientinfo, fs.netdfssetclientinfo, lmdfs/NetDfsSetClientInfo, netmgmt.netdfssetclientinfo
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsSetClientInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsSetClientInfo function


## -description


Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.


## -parameters




### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace; <i>DomDfsname</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

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
<a href="https://msdn.microsoft.com/506aaf68-2f23-4dd2-b43c-aeb86334a3d8">DFS_INFO_101</a> structure.



#### 102

Set the local DFS link time-out. The <i>Buffer</i> parameter points to a 
<a href="https://msdn.microsoft.com/ca4da0a2-d5b3-4ad6-bc00-6629b9bf13e7">DFS_INFO_102</a> structure. For more information, see the following Remarks section.


### -param Buffer [in]

Pointer to a buffer that contains the information to be set. The format of this information depends on the value of the <i>Level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have Administrator privilege on the DFS server. For more information about calling functions that require administrator privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

Setting the time-out to zero may not immediately delete the local cached copy of the DFS link, because threads may be referencing the entry.

Because there is only one time-out on a DFS link, the <i>ServerName</i> and <i>ShareName</i> parameters are ignored for level 102.

The <b>DFS_STORAGE_STATE_ONLINE</b> and <b>DFS_STORAGE_STATE_OFFLINE</b> bits will be ignored. The <b>DFS_STORAGE_STATE_ACTIVE</b> bit is valid only if no files are open to the active computer.




## -see-also




<a href="https://msdn.microsoft.com/506aaf68-2f23-4dd2-b43c-aeb86334a3d8">DFS_INFO_101</a>



<a href="https://msdn.microsoft.com/ca4da0a2-d5b3-4ad6-bc00-6629b9bf13e7">DFS_INFO_102</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

