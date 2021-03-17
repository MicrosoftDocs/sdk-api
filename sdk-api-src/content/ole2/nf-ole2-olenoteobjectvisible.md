---
UID: NF:ole2.OleNoteObjectVisible
title: OleNoteObjectVisible function (ole2.h)
description: Increments or decrements an external reference that keeps an object in the running state.
helpviewer_keywords: ["OleNoteObjectVisible","OleNoteObjectVisible function [COM]","_ole_OleNoteObjectVisible","com.olenoteobjectvisible","ole2/OleNoteObjectVisible"]
old-location: com\olenoteobjectvisible.htm
tech.root: com
ms.assetid: f140f068-3115-4389-b67b-6d41d12f7525
ms.date: 12/05/2018
ms.keywords: OleNoteObjectVisible, OleNoteObjectVisible function [COM], _ole_OleNoteObjectVisible, com.olenoteobjectvisible, ole2/OleNoteObjectVisible
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleNoteObjectVisible
 - ole2/OleNoteObjectVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleNoteObjectVisible
---

# OleNoteObjectVisible function


## -description

Increments or decrements an external reference that keeps an object in the running state.

## -parameters

### -param pUnknown [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object that is to be locked or unlocked.

### -param fVisible [in]

Whether the object is visible. If <b>TRUE</b>, OLE increments the reference count to hold the object visible and alive regardless of external or internal <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> operations, registrations, or revocation. If <b>FALSE</b>, OLE releases its hold (decrements the reference count) and the object can be closed.

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

The <b>OleNoteObjectVisible</b> function calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a> function. It is provided as a separate function to reinforce the need to lock an object when it becomes visible to the user and to release the object when it becomes invisible. This creates a strong lock on behalf of the user to ensure that the object cannot be closed by its container while it is visible.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>