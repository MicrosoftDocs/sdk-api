---
UID: NF:rpcnsi.RpcNsEntryObjectInqBeginA
title: RpcNsEntryObjectInqBeginA function
author: windows-sdk-content
description: The RpcNsEntryObjectInqBegin function creates an inquiry context for the objects of a name-service database entry.
old-location: rpc\rpcnsentryobjectinqbegin.htm
tech.root: rpc
ms.assetid: dc667dc3-0812-43d5-adc2-aa29ee67f045
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcNsEntryObjectInqBegin, RpcNsEntryObjectInqBegin function [RPC], RpcNsEntryObjectInqBeginA, RpcNsEntryObjectInqBeginW, _rpc_rpcnsentryobjectinqbegin, rpc.rpcnsentryobjectinqbegin, rpcnsi/RpcNsEntryObjectInqBegin, rpcnsi/RpcNsEntryObjectInqBeginA, rpcnsi/RpcNsEntryObjectInqBeginW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsEntryObjectInqBeginW (Unicode) and RpcNsEntryObjectInqBeginA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsEntryObjectInqBegin
 - RpcNsEntryObjectInqBeginA
 - RpcNsEntryObjectInqBeginW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsEntryObjectInqBeginA function


## -description


The 
<b>RpcNsEntryObjectInqBegin</b> function creates an inquiry context for the objects of a name-service database entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax to use in <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param EntryName

Pointer to the name-service database entry name for which object UUIDs are to be viewed.


### -param InquiryContext

Returns a pointer to a name-service handle for use with the 
<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a> and 
<a href="https://msdn.microsoft.com/de1ed214-1018-498a-81a9-7932d4eead0b">RpcNsEntryObjectInqDone</a> functions.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsEntryObjectInqBegin</b> function creates an inquiry context for viewing the object UUIDs exported to <i>EntryName</i>.

Before calling the 
<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a> function, the application must first call 
<b>RpcNsEntryObjectInqBegin</b> to create an inquiry context.

When finished viewing the object UUIDs, the application calls the 
<a href="https://msdn.microsoft.com/de1ed214-1018-498a-81a9-7932d4eead0b">RpcNsEntryObjectInqDone</a> function to delete the inquiry context.




## -see-also




<a href="https://msdn.microsoft.com/c89d04d7-f607-48cc-8cb6-b6aebab41671">RpcNsBindingExport</a>



<a href="https://msdn.microsoft.com/de1ed214-1018-498a-81a9-7932d4eead0b">RpcNsEntryObjectInqDone</a>



<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a>
 

 

