---
UID: NF:rpcnsi.RpcNsBindingUnexportPnPW
title: RpcNsBindingUnexportPnPW function (rpcnsi.h)
description: The RpcNsBindingUnexportPnP function removes the binding handles for Plug and Play interfaces and objects from an entry in the name-service database. (Unicode)
helpviewer_keywords: ["RpcNsBindingUnexportPnP", "RpcNsBindingUnexportPnP function [RPC]", "RpcNsBindingUnexportPnPW", "_rpc_rpcnsbindingunexportpnp", "rpc.rpcnsbindingunexportpnp", "rpcnsi/RpcNsBindingUnexportPnP", "rpcnsi/RpcNsBindingUnexportPnPW"]
old-location: rpc\rpcnsbindingunexportpnp.htm
tech.root: Rpc
ms.assetid: b19d9c18-b2fa-45da-b55f-583483c4d540
ms.date: 12/05/2018
ms.keywords: RpcNsBindingUnexportPnP, RpcNsBindingUnexportPnP function [RPC], RpcNsBindingUnexportPnPA, RpcNsBindingUnexportPnPW, _rpc_rpcnsbindingunexportpnp, rpc.rpcnsbindingunexportpnp, rpcnsi/RpcNsBindingUnexportPnP, rpcnsi/RpcNsBindingUnexportPnPA, rpcnsi/RpcNsBindingUnexportPnPW
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsBindingUnexportPnPW
 - rpcnsi/RpcNsBindingUnexportPnPW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsBindingUnexportPnP
 - RpcNsBindingUnexportPnPA
 - RpcNsBindingUnexportPnPW
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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingUnexportPnP</b> function allows a server application to remove the binding handles and object UUIDs of Plug and Play-compatible resources from a name service database entry. A server application can unexport the specified interface and objects in a single call to 
<b>RpcNsBindingUnexportPnP</b>, or it can unexport them separately. Only the binding handles that match the interface UUID and the major and minor interface version numbers found in the <i>IfSpec</i> parameter are unexported.





> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingUnexportPnP as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa">RpcNsBindingExportPnP</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a>
