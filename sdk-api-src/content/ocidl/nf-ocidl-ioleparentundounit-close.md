---
UID: NF:ocidl.IOleParentUndoUnit.Close
title: IOleParentUndoUnit::Close (ocidl.h)
description: Closes the specified parent undo unit. (IOleParentUndoUnit.Close)
helpviewer_keywords: ["Close","Close method [COM]","Close method [COM]","IOleParentUndoUnit interface","IOleParentUndoUnit interface [COM]","Close method","IOleParentUndoUnit.Close","IOleParentUndoUnit::Close","_ole_ioleparentundounit_close","com.ioleparentundounit_close","ocidl/IOleParentUndoUnit::Close"]
old-location: com\ioleparentundounit_close.htm
tech.root: com
ms.assetid: dcfe1962-c40f-4d3f-ae6a-b70755adebe8
ms.date: 12/05/2018
ms.keywords: Close, Close method [COM], Close method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],Close method, IOleParentUndoUnit.Close, IOleParentUndoUnit::Close, _ole_ioleparentundounit_close, com.ioleparentundounit_close, ocidl/IOleParentUndoUnit::Close
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleParentUndoUnit::Close
 - ocidl/IOleParentUndoUnit::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleParentUndoUnit.Close
---

# IOleParentUndoUnit::Close


## -description

Closes the specified parent undo unit.

## -parameters

### -param pPUU [in]

An <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a> pointer to the currently open parent unit to be closed.

### -param fCommit [in]

Indicates whether to keep or discard the unit. If <b>TRUE</b>, the unit is kept in the collection. If <b>FALSE</b>, the unit is discarded. This parameter is used to allow the client to discard an undo unit under construction if an error or a cancellation occurs.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The parent undo unit did not have an open child and it was successfully closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If pPUU does not match the currently open parent undo unit, then implementations of this method should return E_INVALIDARG without changing any internal state unless the parent unit is blocked.

</td>
</tr>
</table>

## -remarks

A parent undo unit knows it is being closed when it returns S_FALSE from this method. At that time, it should terminate any communication with other objects which may be giving data to it through private interfaces.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
An error return indicates a fatal error condition.

The parent unit or undo manager must accept the undo unit if <i>fCommit</i> is <b>TRUE</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
To process a close request, a parent undo unit first checks to see if it has an open child unit. If it does not, it returns S_FALSE.

If it does have a child unit open, it calls the <b>IOleParentUndoUnit::Close</b> method on the child. If the child returns S_FALSE, then the parent undo unit verifies that <i>pPUU</i> points to the child unit, and closes that child undo unit. If the child returns S_OK then it handled the close internally and its parent should do nothing.

If the parent unit is blocked, it should check the <i>pPUU</i> parameter to determine the appropriate return code. If <i>pPUU</i> is pointing to itself, then it should return S_FALSE.

Otherwise, it should return S_OK; the <i>fCommit</i> parameter is ignored; and no action is taken.

If <i>pPUU</i> does not match the currently open parent undo unit, then implementations of this method should return E_INVALIDARG without changing any internal state. The only exception to this is if the unit is blocked.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a>
