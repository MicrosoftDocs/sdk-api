---
UID: NF:ocidl.IOleUndoUnit.Do
title: IOleUndoUnit::Do (ocidl.h)
description: Instructs the undo unit to carry out its action. Note that if it contains child undo units, it must call their Do methods as well.
helpviewer_keywords: ["Do","Do method [COM]","Do method [COM]","IOleUndoUnit interface","IOleUndoUnit interface [COM]","Do method","IOleUndoUnit.Do","IOleUndoUnit::Do","_ole_ioleundounit_do","com.ioleundounit_do","ocidl/IOleUndoUnit::Do"]
old-location: com\ioleundounit_do.htm
tech.root: com
ms.assetid: 5f087779-ef92-41c9-94e6-61d07d5731a7
ms.date: 12/05/2018
ms.keywords: Do, Do method [COM], Do method [COM],IOleUndoUnit interface, IOleUndoUnit interface [COM],Do method, IOleUndoUnit.Do, IOleUndoUnit::Do, _ole_ioleundounit_do, com.ioleundounit_do, ocidl/IOleUndoUnit::Do
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
 - IOleUndoUnit::Do
 - ocidl/IOleUndoUnit::Do
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
 - IOleUndoUnit.Do
---

# IOleUndoUnit::Do


## -description

Instructs the undo unit to carry out its action. Note that if it contains child undo units, it must call their Do methods as well.

## -parameters

### -param pUndoManager [in]

A pointer to the undo manager. See <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>.

## -returns

This method returns S_OK on success.

## -remarks

The undo unit is responsible for carrying out its action. Performing its own undo action results in another action that can potentially be reversed. However, if <i>pUndoManager</i> is <b>NULL</b>, the undo unit should perform its undo action but should not attempt to put anything on the redo or undo stack.

If <i>pUndoManager</i> is not <b>NULL</b>, then the unit is required to put a corresponding unit on the redo or undo stack. As a result, this method either moves itself to the redo or undo stack, or it creates a new undo unit and adds it to the appropriate stack. After creating a new undo unit, this undo unit calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-open">IOleUndoManager::Open</a> or <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a>. The undo manager will put the new undo unit on the undo or redo stack depending on its current state.

A parent unit must pass to its children the same undo manager, possibly <b>NULL</b>, that was given to the parent. It is permissible, but not necessary, when <i>pUndoManager</i> is <b>NULL</b> to open a parent unit on the redo or undo stack as long as it is not committed. A blocked parent unit ensures that nothing is added to the stack by child units.

If this undo unit is a parent unit, it should put itself on the redo or undo stack before calling the <b>Do</b> method on its children.

After calling this method, the undo manager must release the undo unit.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
See the <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a> interface for error handling strategies for undo units. The error handling strategy affects the implementation of this method, particularly for parent units.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-open">IOleUndoManager::Open</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>