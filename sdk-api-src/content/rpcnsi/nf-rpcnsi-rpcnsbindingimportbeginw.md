---
UID: NF:rpcnsi.RpcNsBindingImportBeginW
title: RpcNsBindingImportBeginW function (rpcnsi.h)
description: The RpcNsBindingImportBegin function creates an import context for importing client-compatible binding handles for servers that offer the specified interface and object. (Unicode)
helpviewer_keywords: ["RpcNsBindingImportBegin", "RpcNsBindingImportBegin function [RPC]", "RpcNsBindingImportBeginW", "_rpc_rpcnsbindingimportbegin", "rpc.rpcnsbindingimportbegin", "rpcnsi/RpcNsBindingImportBegin", "rpcnsi/RpcNsBindingImportBeginW"]
old-location: rpc\rpcnsbindingimportbegin.htm
tech.root: Rpc
ms.assetid: 8dca0490-72aa-41e0-b747-863d53a705ea
ms.date: 12/05/2018
ms.keywords: RpcNsBindingImportBegin, RpcNsBindingImportBegin function [RPC], RpcNsBindingImportBeginA, RpcNsBindingImportBeginW, _rpc_rpcnsbindingimportbegin, rpc.rpcnsbindingimportbegin, rpcnsi/RpcNsBindingImportBegin, rpcnsi/RpcNsBindingImportBeginA, rpcnsi/RpcNsBindingImportBeginW
req.header: rpcnsi.h
req.include-header: Rpc.h
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsBindingImportBeginW
 - rpcnsi/RpcNsBindingImportBeginW
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
 - RpcNsBindingImportBegin
 - RpcNsBindingImportBeginA
 - RpcNsBindingImportBeginW
---

# RpcNsBindingImportBeginW function


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
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a> and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportdone">RpcNsBindingImportDone</a> functions.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Before calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a> function, the client application must first call 
<b>RpcNsBindingImportBegin</b> to create an import context. The parameters to this function control the operation of the 
<b>RpcNsBindingImportNext</b> function.

When finished importing binding handles, the client application calls the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportdone">RpcNsBindingImportDone</a> function to delete the import context.





> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingImportBegin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportdone">RpcNsBindingImportDone</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>
