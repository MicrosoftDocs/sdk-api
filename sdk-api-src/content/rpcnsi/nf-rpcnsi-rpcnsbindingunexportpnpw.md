---
UID: NF:rpcnsi.RpcNsBindingUnexportPnPW
title: RpcNsBindingUnexportPnPW function
author: windows-sdk-content
description: The RpcNsBindingUnexportPnP function removes the binding handles for Plug and Play interfaces and objects from an entry in the name-service database.
old-location: rpc\rpcnsbindingunexportpnp.htm
old-project: Rpc
ms.assetid: b19d9c18-b2fa-45da-b55f-583483c4d540
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: RpcNsBindingUnexportPnP, RpcNsBindingUnexportPnP function [RPC], RpcNsBindingUnexportPnPA, RpcNsBindingUnexportPnPW, _rpc_rpcnsbindingunexportpnp, rpc.rpcnsbindingunexportpnp, rpcnsi/RpcNsBindingUnexportPnP, rpcnsi/RpcNsBindingUnexportPnPA, rpcnsi/RpcNsBindingUnexportPnPW
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
req.unicode-ansi: RpcNsBindingUnexportPnPW (Unicode) and RpcNsBindingUnexportPnPA (ANSI)
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
-	RpcNsBindingUnexportPnP
-	RpcNsBindingUnexportPnPA
-	RpcNsBindingUnexportPnPW
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcNsBindingUnexportPnPW function


## -description


The 
<b>RpcNsBindingUnexportPnP</b> function removes the binding handles for Plug and Play interfaces and objects from an entry in the name-service database.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param EntryName

Pointer to the entry name from which to remove binding handles and object UUIDs.


### -param IfSpec

Interface specification for the binding handles to be removed from the name service database. A null parameter value indicates not to unexport any binding handles (only object UUIDs are to be unexported).


### -param ObjectVector

TBD




#### - ObjectUuidVec

Pointer to a vector of object UUIDs that the server no longer wants to offer. The application constructs this vector. A null value indicates there are no object UUIDs to unexport (only binding handles are to be unexported).


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
<dt><b>RPC_S_INVALID_VERS_OPTION</b></dt>
</dl>
</td>
<td width="60%">
The version option is invalid.

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
The name syntax is unsupported.

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
<dt><b>RPC_S_INTERFACE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The interface was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_ALL_OBJS_UNEXPORTED</b></dt>
</dl>
</td>
<td width="60%">
Not all objects unexported.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsBindingUnexportPnP</b> function allows a server application to remove the binding handles and object UUIDs of Plug and Play-compatible resources from a name service database entry. A server application can unexport the specified interface and objects in a single call to 
<b>RpcNsBindingUnexportPnP</b>, or it can unexport them separately. Only the binding handles that match the interface UUID and the major and minor interface version numbers found in the <i>IfSpec</i> parameter are unexported.




## -see-also




<a href="https://msdn.microsoft.com/01440165-ab04-447a-9a39-9e91743aba65">RpcNsBindingExportPnP</a>



<a href="https://msdn.microsoft.com/70662e7e-7a81-4953-9814-e29b46422c5b">RpcNsBindingUnexport</a>
 

 

