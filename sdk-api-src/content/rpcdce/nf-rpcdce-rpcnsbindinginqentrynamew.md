---
UID: NF:rpcdce.RpcNsBindingInqEntryNameW
title: RpcNsBindingInqEntryNameW function
author: windows-sdk-content
description: The RpcNsBindingInqEntryName function returns the entry name from which the binding handle came.
old-location: rpc\rpcnsbindinginqentryname.htm
tech.root: rpc
ms.assetid: fff87506-4c3f-47cb-8130-78e46e906bf0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RpcNsBindingInqEntryName, RpcNsBindingInqEntryName function [RPC], RpcNsBindingInqEntryNameA, RpcNsBindingInqEntryNameW, _rpc_rpcnsbindinginqentryname, rpc.rpcnsbindinginqentryname, rpcdce/RpcNsBindingInqEntryName, rpcdce/RpcNsBindingInqEntryNameA, rpcdce/RpcNsBindingInqEntryNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsBindingInqEntryNameW function


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
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsBindingInqEntryName</b> function returns the name of the name service–database entry name from which a client compatible–binding handle came.

The RPC run-time library allocates memory for the string returned in the <i>EntryName</i> parameter. The application is responsible for calling the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function to deallocate that memory.

An entry name is associated only with binding handles returned from the 
<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>, 
<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>, and 
<a href="https://msdn.microsoft.com/1acdd266-9ca2-43d4-b677-7c30b4dca4ee">RpcNsBindingSelect</a> functions.

If the binding handle specified in the <i>Binding</i> parameter was not returned from a name-service database entry (for example, if the binding handle was created by calling 
<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>), 
<b>RpcNsBindingInqEntryName</b> returns an empty string ("\0") and an RPC_S_NO_ENTRY_NAME status code.




## -see-also




<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>



<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>



<a href="https://msdn.microsoft.com/1acdd266-9ca2-43d4-b677-7c30b4dca4ee">RpcNsBindingSelect</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

