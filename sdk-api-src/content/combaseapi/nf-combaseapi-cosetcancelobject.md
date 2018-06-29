---
UID: NF:combaseapi.CoSetCancelObject
title: CoSetCancelObject function
author: windows-sdk-content
description: Sets (registers) or resets (unregisters) a cancel object for use during subsequent cancel operations on the current thread.
old-location: com\cosetcancelobject.htm
old-project: com
ms.assetid: 0978e252-2206-4597-abf2-fe0dac32efc4
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CoSetCancelObject, CoSetCancelObject function [COM], _com_CoSetCancelObject, com.cosetcancelobject, combaseapi/CoSetCancelObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoSetCancelObject
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoSetCancelObject function


## -description


Sets (registers) or resets (unregisters) a cancel object for use during subsequent cancel operations on the current thread.


## -parameters




### -param pUnk [in, optional]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the cancel object to be set or reset on the current thread. If this parameter is <b>NULL</b>, the topmost cancel object is reset.


## -returns



This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The cancel object was successfully set or reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The cancel object cannot be set or reset at this time because of a block on cancel operations.


</td>
</tr>
</table>
 




## -remarks



For objects that support standard marshaling, the proxy object begins marshaling a method call by calling <b>CoSetCancelObject</b> to register a cancel object for the current thread.

<b>CoSetCancelObject</b> calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for <a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a> on the cancel object. If the cancel object does not implement <b>ICancelMethodCalls</b>, <b>CoSetCancelObject</b> fails with E_NOINTERFACE. To disable cancel operations on a custom-marshaled interface, the implementation of <a href="https://msdn.microsoft.com/3c3fdcec-10f1-4fbf-af93-582e7390decf">ICancelMethodCalls::Cancel</a> should do nothing but return E_NOTIMPL, E_FAIL, or some other appropriate value.

<b>CoSetCancelObject</b> calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on objects that it registers and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on objects that it unregisters.

<b>CoSetCancelObject</b> does not set or reset cancel objects for asynchronous methods.




## -see-also




<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 

