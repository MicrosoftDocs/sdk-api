---
UID: NF:rpcdce.RpcNsBindingInqEntryNameA
title: RpcNsBindingInqEntryNameA function (rpcdce.h)
description: The RpcNsBindingInqEntryName function returns the entry name from which the binding handle came. (RpcNsBindingInqEntryNameA)
helpviewer_keywords: ["RpcNsBindingInqEntryNameA", "rpcdce/RpcNsBindingInqEntryNameA"]
old-location: rpc\rpcnsbindinginqentryname.htm
tech.root: Rpc
ms.assetid: fff87506-4c3f-47cb-8130-78e46e906bf0
ms.date: 12/05/2018
ms.keywords: RpcNsBindingInqEntryName, RpcNsBindingInqEntryName function [RPC], RpcNsBindingInqEntryNameA, RpcNsBindingInqEntryNameW, _rpc_rpcnsbindinginqentryname, rpc.rpcnsbindinginqentryname, rpcdce/RpcNsBindingInqEntryName, rpcdce/RpcNsBindingInqEntryNameA, rpcdce/RpcNsBindingInqEntryNameW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingInqEntryNameW (Unicode) and RpcNsBindingInqEntryNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsBindingInqEntryNameA
 - rpcdce/RpcNsBindingInqEntryNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcNsBindingInqEntryName
 - RpcNsBindingInqEntryNameA
 - RpcNsBindingInqEntryNameW
---

# RpcNsBindingInqEntryNameA function


## -description

The 
<b>RpcNsBindingInqEntryName</b> function returns the entry name from which the binding handle came.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param Binding

Binding handle whose name-service database entry name is returned.

### -param EntryNameSyntax

Syntax used in <i>EntryName</i>. 




To use the syntax specified in the registry value entry

<b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Returns the address of a pointer to the name of the name-service database entry in which <i>Binding</i> was found. 




Specify a null value to prevent 
<b>RpcNsBindingInqEntryName</b> from returning the <i>EntryName</i> parameter. In this case, the application does not call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.

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
<dt><b>RPC_S_NO_ENTRY_NAME</b></dt>
</dl>
</td>
<td width="60%">
No entry name for binding.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingInqEntryName</b> function returns the name of the name service–database entry name from which a client compatible–binding handle came.

The RPC run-time library allocates memory for the string returned in the <i>EntryName</i> parameter. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function to deallocate that memory.

An entry name is associated only with binding handles returned from the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>, 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>, and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a> functions.

If the binding handle specified in the <i>Binding</i> parameter was not returned from a name-service database entry (for example, if the binding handle was created by calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>), 
<b>RpcNsBindingInqEntryName</b> returns an empty string ("\0") and an RPC_S_NO_ENTRY_NAME status code.





> [!NOTE]
> The rpcdce.h header defines RpcNsBindingInqEntryName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
