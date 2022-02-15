---
UID: NN:ocidl.IOleUndoUnit
title: IOleUndoUnit (ocidl.h)
description: Serves as the main interface on an undo unit. An undo unit encapsulates the information necessary to undo or redo a single action.
helpviewer_keywords: ["IOleUndoUnit","IOleUndoUnit interface [COM]","IOleUndoUnit interface [COM]","described","_ole_ioleundounit","com.ioleundounit","ocidl/IOleUndoUnit"]
old-location: com\ioleundounit.htm
tech.root: com
ms.assetid: 0822c894-b96c-4b69-94d2-b052dff81f6e
ms.date: 12/05/2018
ms.keywords: IOleUndoUnit, IOleUndoUnit interface [COM], IOleUndoUnit interface [COM],described, _ole_ioleundounit, com.ioleundounit, ocidl/IOleUndoUnit
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
 - IOleUndoUnit
 - ocidl/IOleUndoUnit
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
 - IOleUndoUnit
---

# IOleUndoUnit interface


## -description

Serves as the main interface on an undo unit. An undo unit encapsulates the information necessary to undo or redo a single action.

When an object's state changes and it needs to create an undo unit, it first needs to know what parent units are open. It calls the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getopenparentstate">IOleUndoManager::GetOpenParentState</a> method to determine this. If the call returns S_FALSE, then there is no enabling parent. If the call returns S_OK but the UAS_NOPARENTENABLE flag is set, then the open parent is a disabling parent. In either of these cases, the object calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-discardfrom">IOleUndoManager::DiscardFrom</a>(NULL) on the undo manager and skips creating the undo unit.

If the method returns S_OK, but the UAS_BLOCKED flag is set, then the open parent is a blocking parent. The object does not need to create an undo unit, since it would be immediately discarded. If the return value is S_OK and neither of the bit flags are set, then the object creates the undo unit and calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a> on the undo manager.

The object should retain a pointer to the undo manager.

## -inheritance

The <b>IOleUndoUnit</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleUndoUnit</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>
