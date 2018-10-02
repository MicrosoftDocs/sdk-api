---
UID: NF:tdh.TdhGetWppMessage
title: TdhGetWppMessage function
author: windows-sdk-content
description: Retrieves the formatted WPP message embedded into an EVENT_RECORD structure.
old-location: etw\tdhgetwppmessage.htm
tech.root: ETW
ms.assetid: e4daf7fb-4512-41bd-b7b9-3f9f1cd15037
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TdhGetWppMessage, TdhGetWppMessage function [ETW], etw.tdhgetwppmessage, tdh/TdhGetWppMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhGetWppMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TdhGetWppMessage function


## -description


Retrieves the formatted WPP message embedded into an <a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a> structure.


## -parameters




### -param Handle [in]

Type: <b>TDH_HANDLE</b>

A valid decoding handle.


### -param EventRecord [in]

Type: <b><a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">PEVENT_RECORD</a></b>

The event record passed to your <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback.


### -param BufferSize [in, out]

Type: <b>PULONG</b>

Size of the <i>Buffer</i> parameter, in bytes.


### -param Buffer [out]

Type: <b>PBYTE</b>

User-allocated buffer that receives the property data.


## -returns



Type: <b>ULONG</b>

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified property was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>BufferSize</i> is too small. To get the required buffer size, call <a href="https://msdn.microsoft.com/52b034db-b08b-4c79-973f-33800ca866f5">TdhGetPropertySize</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
</table>
 




## -remarks



To retrieve a specific property instead of the decoded event message without specifying a property name, call <a href="https://msdn.microsoft.com/a9c5ed0f-af6f-4500-9ef7-bc60b8911ea0">TdhGetWppProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a>



<a href="https://msdn.microsoft.com/52b034db-b08b-4c79-973f-33800ca866f5">TdhGetPropertySize</a>



<a href="https://msdn.microsoft.com/a9c5ed0f-af6f-4500-9ef7-bc60b8911ea0">TdhGetWppProperty</a>
 

 

