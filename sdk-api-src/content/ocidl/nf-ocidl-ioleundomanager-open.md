---
UID: NF:ocidl.IOleUndoManager.Open
title: IOleUndoManager::Open (ocidl.h)
description: Opens a new parent undo unit, which becomes part of its containing unit's undo stack.
helpviewer_keywords: ["IOleUndoManager interface [COM]","Open method","IOleUndoManager.Open","IOleUndoManager::Open","Open","Open method [COM]","Open method [COM]","IOleUndoManager interface","_ole_ioleundomanager_open","com.ioleundomanager_open","ocidl/IOleUndoManager::Open"]
old-location: com\ioleundomanager_open.htm
tech.root: com
ms.assetid: b494d5b9-5def-4249-8b6d-37b26993cc24
ms.date: 12/05/2018
ms.keywords: IOleUndoManager interface [COM],Open method, IOleUndoManager.Open, IOleUndoManager::Open, Open, Open method [COM], Open method [COM],IOleUndoManager interface, _ole_ioleundomanager_open, com.ioleundomanager_open, ocidl/IOleUndoManager::Open
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
 - IOleUndoManager::Open
 - ocidl/IOleUndoManager::Open
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
 - IOleUndoManager.Open
---

# IOleUndoManager::Open


## -description

Opens a new parent undo unit, which becomes part of its containing unit's undo stack.

## -parameters

### -param pPUU [in]

An <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a> pointer to the parent undo unit to be opened.

## -returns

This method returns S_OK if the parent undo unit was successfully opened or if a currently open unit is blocked. If the undo manager is currently disabled, it will return S_OK and do nothing else.

## -remarks

This method is implemented the same as <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-open">IOleParentUndoUnit::Open</a>. The specified parent unit is created and remains open. The undo manager then calls the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a> or <b>IOleUndoManager::Open</b> methods on this parent unit to add new units to it. This parent unit receives any additional undo units until its <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-close">IOleUndoManager::Close</a> method is called.

The parent unit specified by <i>pPUU</i> is not added to the undo stack until its <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-close">IOleUndoManager::Close</a> method is called with the <i>fCommit</i> parameter set to <b>TRUE</b>.

The parent undo unit or undo manager must contain any undo unit given to it unless it is blocked. If it is blocked, it must return S_OK but should do nothing else.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>