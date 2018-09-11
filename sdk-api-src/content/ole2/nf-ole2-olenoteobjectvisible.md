---
UID: NF:ole2.OleNoteObjectVisible
title: OleNoteObjectVisible function
author: windows-sdk-content
description: Increments or decrements an external reference that keeps an object in the running state.
old-location: com\olenoteobjectvisible.htm
tech.root: com
ms.assetid: f140f068-3115-4389-b67b-6d41d12f7525
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: OleNoteObjectVisible, OleNoteObjectVisible function [COM], _ole_OleNoteObjectVisible, com.olenoteobjectvisible, ole2/OleNoteObjectVisible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleNoteObjectVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleNoteObjectVisible function


## -description


Increments or decrements an external reference that keeps an object in the running state.




## -parameters




### -param pUnknown [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object that is to be locked or unlocked.


### -param fVisible [in]

Whether the object is visible. If <b>TRUE</b>, OLE increments the reference count to hold the object visible and alive regardless of external or internal <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> operations, registrations, or revocation. If <b>FALSE</b>, OLE releases its hold (decrements the reference count) and the object can be closed.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>OleNoteObjectVisible</b> function calls the <a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a> function. It is provided as a separate function to reinforce the need to lock an object when it becomes visible to the user and to release the object when it becomes invisible. This creates a strong lock on behalf of the user to ensure that the object cannot be closed by its container while it is visible.





## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>
 

 

