---
UID: NF:rpcnsi.RpcNsBindingImportBeginA
title: RpcNsBindingImportBeginA function
author: windows-sdk-content
description: The RpcNsBindingImportBegin function creates an import context for importing client-compatible binding handles for servers that offer the specified interface and object.
old-location: rpc\rpcnsbindingimportbegin.htm
old-project: Rpc
ms.assetid: 8dca0490-72aa-41e0-b747-863d53a705ea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcNsBindingImportBegin, RpcNsBindingImportBegin function [RPC], RpcNsBindingImportBeginA, RpcNsBindingImportBeginW, _rpc_rpcnsbindingimportbegin, rpc.rpcnsbindingimportbegin, rpcnsi/RpcNsBindingImportBegin, rpcnsi/RpcNsBindingImportBeginA, rpcnsi/RpcNsBindingImportBeginW
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
req.unicode-ansi: RpcNsBindingImportBeginW (Unicode) and RpcNsBindingImportBeginA (ANSI)
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
 - RpcNsBindingImportBegin
 - RpcNsBindingImportBeginA
 - RpcNsBindingImportBeginW
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: ADAM
---

# RpcNsBindingImportBeginA function


## -description


The 
<b>RpcNsBindingImportBegin</b> function creates an import context for importing client-compatible binding handles for servers that offer the specified interface and object.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, specify RPC_C_NS_SYNTAX_DEFAULT.


### -param EntryName

Pointer to an entry name at which the search for compatible binding handles begins. 




To use the entry name specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultEntry</b>, provide a null pointer or an empty string. In this case, the <i>EntryNameSyntax</i> parameter is ignored and the run-time library uses the default syntax.


### -param IfSpec

Stub-generated data structure indicating the interface to import. If the interface specification has not been exported or is of no concern to the caller, specify a null value for this parameter. In this case, the bindings returned are only guaranteed to be of a compatible and supported protocol sequence and to contain the specified object UUID. The contacted server might not support the desired interface.


### -param ObjUuid

Pointer to an optional object UUID. 




For a nonzero UUID, compatible binding handles are returned from an entry only if the server has exported the specified object UUID.

When <i>ObjUuid</i> has a null pointer value or a nil UUID, the returned binding handles contain one of the object UUIDs exported by the compatible server. If the server did not export any object UUIDs, the returned compatible binding handles contain a nil object UUID.


### -param ImportContext

Name-service handle returned for use with the 
<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a> and 
<a href="https://msdn.microsoft.com/093c988a-5d88-45b5-b69a-f26962118fdb">RpcNsBindingImportDone</a> functions.


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
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name exceeds the maximum length.

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
<dt><b>RPC_S_INVALID_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid object.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Before calling the 
<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a> function, the client application must first call 
<b>RpcNsBindingImportBegin</b> to create an import context. The parameters to this function control the operation of the 
<b>RpcNsBindingImportNext</b> function.

When finished importing binding handles, the client application calls the 
<a href="https://msdn.microsoft.com/093c988a-5d88-45b5-b69a-f26962118fdb">RpcNsBindingImportDone</a> function to delete the import context.




## -see-also




<a href="https://msdn.microsoft.com/093c988a-5d88-45b5-b69a-f26962118fdb">RpcNsBindingImportDone</a>



<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>
 

 

