---
UID: NF:rpcnsi.RpcNsBindingExportPnPW
title: RpcNsBindingExportPnPW function (rpcnsi.h)
description: The RpcNsBindingExportPnP function establishes a name-service database entry with multiple binding handles and multiple objects for a server that supports Plug and Play. (Unicode)
helpviewer_keywords: ["RpcNsBindingExportPnP", "RpcNsBindingExportPnP function [RPC]", "RpcNsBindingExportPnPW", "_rpc_rpcnsbindingexportpnp", "rpc.rpcnsbindingexportpnp", "rpcnsi/RpcNsBindingExportPnP", "rpcnsi/RpcNsBindingExportPnPW"]
old-location: rpc\rpcnsbindingexportpnp.htm
tech.root: Rpc
ms.assetid: 01440165-ab04-447a-9a39-9e91743aba65
ms.date: 12/05/2018
ms.keywords: RpcNsBindingExportPnP, RpcNsBindingExportPnP function [RPC], RpcNsBindingExportPnPA, RpcNsBindingExportPnPW, _rpc_rpcnsbindingexportpnp, rpc.rpcnsbindingexportpnp, rpcnsi/RpcNsBindingExportPnP, rpcnsi/RpcNsBindingExportPnPA, rpcnsi/RpcNsBindingExportPnPW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingExportPnPW (Unicode) and RpcNsBindingExportPnPA (ANSI)
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
 - RpcNsBindingExportPnPW
 - rpcnsi/RpcNsBindingExportPnPW
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
 - RpcNsBindingExportPnP
 - RpcNsBindingExportPnPA
 - RpcNsBindingExportPnPW
---

# RpcNsBindingExportPnPW function


## -description

The 
<b>RpcNsBindingExportPnP</b> function establishes a name-service database entry with multiple binding handles and multiple objects for a server that supports Plug and Play.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the entry name to which binding handles and object UUIDs are exported. You cannot provide a null or empty string. 




To use the entry name specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultEntry</b>, provide a null pointer or an empty string. In this case, the <i>EntryNameSyntax</i> parameter is ignored and the run-time library uses the default syntax.

### -param IfSpec

Stub-generated data structure specifying the interface to export. A null value indicates there are no binding handles to export (only object UUIDs are to be exported) and <i>BindingVec</i> is ignored.

### -param ObjectVector

Pointer to a vector of object UUIDs offered by the server. The server application constructs this vector. A null value indicates there are no object UUIDs to export (only binding handles are to be exported).

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
<dt><b>RPC_S_NOTHING_TO_EXPORT</b></dt>
</dl>
</td>
<td width="60%">
There was nothing to export.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

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
<dt><b>RPC_S_NO_NS_PRIVILEGE</b></dt>
</dl>
</td>
<td width="60%">
No privilege for name-service operation.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingExportPnP</b> function allows a server application to publicly offer an interface in the name-service database that supports Plug and Play bindings for use by any client application.

Note that the server application should not explicitly supply the binding vector when exporting Plug and Play bindings. The bindings are automatically updated when there is a change in the bindings due to a Plug and Play event.





> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingExportPnP as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa">RpcNsBindingUnexportPnP</a>
