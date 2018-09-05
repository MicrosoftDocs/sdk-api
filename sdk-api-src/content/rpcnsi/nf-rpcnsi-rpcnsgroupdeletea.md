---
UID: NF:rpcnsi.RpcNsGroupDeleteA
title: RpcNsGroupDeleteA function
author: windows-sdk-content
description: The RpcNsGroupDelete function deletes a group attribute.
old-location: rpc\rpcnsgroupdelete.htm
old-project: Rpc
ms.assetid: 4455e891-7846-47b5-9283-549c3451b70e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RPC_C_NS_SYNTAX_DCE, RPC_C_NS_SYNTAX_DEFAULT, RpcNsGroupDelete, RpcNsGroupDelete function [RPC], RpcNsGroupDeleteA, RpcNsGroupDeleteW, _rpc_rpcnsgroupdelete, rpc.rpcnsgroupdelete, rpcnsi/RpcNsGroupDelete, rpcnsi/RpcNsGroupDeleteA, rpcnsi/RpcNsGroupDeleteW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupDeleteW (Unicode) and RpcNsGroupDeleteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsGroupDelete
 - RpcNsGroupDeleteA
 - RpcNsGroupDeleteW
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: ADAM
---

# RpcNsGroupDeleteA function


## -description


The 
<b>RpcNsGroupDelete</b> function deletes a group attribute.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param GroupNameSyntax

Integer value that indicates the syntax of <i>GroupName</i>. Can be set to one of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_NS_SYNTAX_DEFAULT"></a><a id="rpc_c_ns_syntax_default"></a><dl>
<dt><b>RPC_C_NS_SYNTAX_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Use the syntax specified in the registry value <b>HKEY_LOCAL_MACHINE\
Software\Microsoft\Rpc\
NameService\
DefaultSyntax
							</b>

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_NS_SYNTAX_DCE"></a><a id="rpc_c_ns_syntax_dce"></a><dl>
<dt><b>RPC_C_NS_SYNTAX_DCE</b></dt>
</dl>
</td>
<td width="60%">
Use DCE syntax.

</td>
</tr>
</table>
 


### -param GroupName

Pointer to the name of the name-service group to delete.


## -returns



This function returns one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ENTRY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The name-service entry was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupDelete</b> function deletes the group attribute from the specified name service–database entry.

Neither the specified name service–database entry nor the group members are deleted.

<div class="alert"><b>Note</b>  This DCE function is not supported by Microsoft Locator. Windows NT and Windows 2000 both support the use of this function, but with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fa32b5e5-1a8a-44f4-aa38-81b024f4db51">RpcNsGroupMbrAdd</a>



<a href="https://msdn.microsoft.com/0301b570-9a03-4f50-89df-3c15d8de246f">RpcNsGroupMbrRemove</a>
 

 

