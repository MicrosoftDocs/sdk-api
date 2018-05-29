---
UID: NF:rpcnsi.RpcNsGroupMbrRemoveW
title: RpcNsGroupMbrRemoveW function
author: windows-sdk-content
description: The RpcNsGroupMbrRemove function removes an entry name from a group.
old-location: rpc\rpcnsgroupmbrremove.htm
old-project: Rpc
ms.assetid: 0301b570-9a03-4f50-89df-3c15d8de246f
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: RpcNsGroupMbrRemove, RpcNsGroupMbrRemove function [RPC], RpcNsGroupMbrRemoveA, RpcNsGroupMbrRemoveW, _rpc_rpcnsgroupmbrremove, rpc.rpcnsgroupmbrremove, rpcnsi/RpcNsGroupMbrRemove, rpcnsi/RpcNsGroupMbrRemoveA, rpcnsi/RpcNsGroupMbrRemoveW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupMbrRemoveW (Unicode) and RpcNsGroupMbrRemoveA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcns4.dll
api_name:
-	RpcNsGroupMbrRemove
-	RpcNsGroupMbrRemoveA
-	RpcNsGroupMbrRemoveW
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcNsGroupMbrRemoveW function


## -description


The 
<b>RpcNsGroupMbrRemove</b> function removes an entry name from a group.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param GroupNameSyntax

Syntax of <i>GroupName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param GroupName

Pointer to the name of the RPC group from which to remove the member name.


### -param MemberNameSyntax

Syntax to use in the <i>MemberName</i> parameter. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param MemberName

Pointer to the name of the member to remove from the RPC group attribute in the entry <i>GroupName</i>.


## -returns



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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_GROUP_MEMBER_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The group member was not found.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupMbrRemove</b> function removes a member from the RPC group attribute in the <i>GroupName</i> parameter.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fa32b5e5-1a8a-44f4-aa38-81b024f4db51">RpcNsGroupMbrAdd</a>
 

 

