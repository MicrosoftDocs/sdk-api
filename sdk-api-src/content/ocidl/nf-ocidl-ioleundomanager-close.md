---
UID: NF:ocidl.IOleUndoManager.Close
title: IOleUndoManager::Close (ocidl.h)
description: Closes the specified parent undo unit. (IOleUndoManager.Close)
helpviewer_keywords: ["Close","Close method [COM]","Close method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","Close method","IOleUndoManager.Close","IOleUndoManager::Close","_ole_ioleundomanager_close","com.ioleundomanager_close","ocidl/IOleUndoManager::Close"]
old-location: com\ioleundomanager_close.htm
tech.root: com
ms.assetid: 4546f270-5cef-42a3-b07a-f0a491e78849
ms.date: 12/05/2018
ms.keywords: Close, Close method [COM], Close method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],Close method, IOleUndoManager.Close, IOleUndoManager::Close, _ole_ioleundomanager_close, com.ioleundomanager_close, ocidl/IOleUndoManager::Close
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
 - IOleUndoManager::Close
 - ocidl/IOleUndoManager::Close
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
 - IOleUndoManager.Close
---

# IOleUndoManager::Close


## -description

Closes the specified parent undo unit.

## -parameters

### -param pPUU [in]

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a> interface for the currently open parent unit to be closed.

### -param fCommit [in]

Indicates whether to keep or discard the unit. If <b>TRUE</b>, the unit is kept in the collection. If <b>FALSE</b>, the unit is discarded. This parameter is used to allow the client to discard an undo unit under construction if an error or a cancellation occurs.

## -returns

This method returns S_OK if the undo manager had an open parent undo unit and it was successfully closed. If the undo manager is disabled, it should immediately return S_OK and do nothing else. Other possible return values include the following.

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
If <i>pPUU</i> does not match the currently open parent undo unit, then implementations of this method should return E_INVALIDARG without changing any internal state unless the parent unit is blocked.

</td>
</tr>
</table>

## -remarks

This method is implemented the same as <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a>. A parent undo unit knows it is being closed when it returns S_FALSE from this method. At that time, it should terminate any communication with other objects which may be giving data to it through private interfaces.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
An error return indicates a fatal error condition.

The parent unit or undo manager must accept the undo unit if <i>fCommit</i> is <b>TRUE</b>.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
To process a close request, a parent undo unit first checks to see if it has an open child unit. If it does not, it returns S_FALSE.

If it does have a child unit open, it calls the <b>IOleUndoManager::Close</b> method on the child. If the child returns S_FALSE, then the parent undo unit verifies that <i>pPUU</i> points to the child unit, and closes that child undo unit. If the child returns S_OK then it handled the close internally and its parent should do nothing.

If the parent unit is blocked, it should check the <i>pPUU</i> parameter to determine the appropriate return code. If <i>pPUU</i> is pointing to itself, then it should return S_FALSE.

Otherwise, it should return S_OK; the <i>fCommit</i> parameter is ignored; and no action is taken.

If <i>pPUU</i> does not match the currently open parent undo unit, then implementations of this method should return E_INVALIDARG without changing any internal state. The only exception to this is if the unit is blocked.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>
