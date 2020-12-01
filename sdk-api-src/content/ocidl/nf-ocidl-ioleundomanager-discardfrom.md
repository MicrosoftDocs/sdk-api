---
UID: NF:ocidl.IOleUndoManager.DiscardFrom
title: IOleUndoManager::DiscardFrom (ocidl.h)
description: Instructs the undo manager to discard the specified undo unit and all undo units below it on the undo or redo stack.
helpviewer_keywords: ["DiscardFrom","DiscardFrom method [COM]","DiscardFrom method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","DiscardFrom method","IOleUndoManager.DiscardFrom","IOleUndoManager::DiscardFrom","_ole_ioleundomanager_discardfrom","com.ioleundomanager_discardfrom","ocidl/IOleUndoManager::DiscardFrom"]
old-location: com\ioleundomanager_discardfrom.htm
tech.root: com
ms.assetid: eb742d04-63cb-4505-bc91-8d87267a3a4a
ms.date: 12/05/2018
ms.keywords: DiscardFrom, DiscardFrom method [COM], DiscardFrom method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],DiscardFrom method, IOleUndoManager.DiscardFrom, IOleUndoManager::DiscardFrom, _ole_ioleundomanager_discardfrom, com.ioleundomanager_discardfrom, ocidl/IOleUndoManager::DiscardFrom
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
 - IOleUndoManager::DiscardFrom
 - ocidl/IOleUndoManager::DiscardFrom
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
 - IOleUndoManager.DiscardFrom
---

# IOleUndoManager::DiscardFrom


## -description

Instructs the undo manager to discard the specified undo unit and all undo units below it on the undo or redo stack.

## -parameters

### -param pUU [in]

An <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a> pointer to the undo unit to be discarded. This parameter can be <b>NULL</b> to discard the entire undo or redo stack. If the parameter is not <b>NULL</b> then the stack will not be discarded.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified undo unit was not found in the stacks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The undo manager is disabled.

</td>
</tr>
</table>

## -remarks

The undo manager first searches the undo stack for the given unit, and if not found there searches the redo stack. After it has been found, the given unit and all below it on the same stack are discarded. The undo unit may be a child of a parent unit contained by the undo manager, as determined by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-findunit">IOleParentUndoUnit::FindUnit</a>. If it is a child unit, then the root unit containing the given unit and all units below it on the appropriate stack are discarded.

If there is an open parent unit and the <b>DiscardFrom</b> method is called and the <i>pUU</i> parameter is <b>NULL</b>, the undo manager should immediately release and discard the open parent unit without calling the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-close">IOleUndoManager::Close</a> first. When the object that opened the parent unit attempts to close it, <b>IOleUndoManager::Close</b> will return S_FALSE. If a parent unit is open, throw it away and discard the stack. If the parent unit is not open, just throw the stack away. If the <i>pUU</i> parameter is not <b>NULL</b>, then any open parent units should be left open.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-findunit">IOleParentUndoUnit::FindUnit</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-close">IOleUndoManager::Close</a>