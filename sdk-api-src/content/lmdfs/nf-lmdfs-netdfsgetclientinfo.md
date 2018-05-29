---
UID: NF:lmdfs.NetDfsGetClientInfo
title: NetDfsGetClientInfo function
author: windows-sdk-content
description: Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.
old-location: dfs\netdfsgetclientinfo.htm
old-project: Dfs
ms.assetid: 065ec002-cb90-4d78-a70c-6ac37f71994f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: 1, 2, 3, 4, NetDfsGetClientInfo, NetDfsGetClientInfo function [Distributed File System], _win32_netdfsgetclientinfo, dfs.netdfsgetclientinfo, fs.netdfsgetclientinfo, lmdfs/NetDfsGetClientInfo
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DFS_TARGET_PRIORITY_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetDfsGetClientInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetDfsGetClientInfo function


## -description


Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.


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

Pointer to a string that specifies the name of the DFS root target or link target server. This parameter is optional.


### -param ShareName [in, optional]

Pointer to a string that specifies the name of the share corresponding to the DFS root target or link target. This parameter is optional.


### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 1

Return the DFS root  or DFS link name. The <i>Buffer</i> parameter points to a 
<a href="https://msdn.microsoft.com/96647570-badd-4925-ab90-054a00ba04c4">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. The <i>Buffer</i> parameter points to a 
<a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and target information. The <i>Buffer</i> parameter points to a 
<a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, <b>GUID</b>, time-out, and target information. The <i>Buffer</i> parameter points to a 
<a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a> structure.


### -param Buffer [out]

Pointer to the address of a buffer that receives the requested information. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required for using the 
<b>NetDfsGetClientInfo</b> function.




## -see-also




<a href="https://msdn.microsoft.com/96647570-badd-4925-ab90-054a00ba04c4">DFS_INFO_1</a>



<a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>



<a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a>



<a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/4c95dffb-a092-45ad-9a3f-37d3abbf4427">NetDfsSetClientInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

