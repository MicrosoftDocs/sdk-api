---
UID: NF:ocidl.IOleParentUndoUnit.GetParentState
title: IOleParentUndoUnit::GetParentState (ocidl.h)
description: Retrieves state information about the innermost open parent undo unit. (IOleParentUndoUnit.GetParentState)
helpviewer_keywords: ["GetParentState","GetParentState method [COM]","GetParentState method [COM]","IOleParentUndoUnit interface","IOleParentUndoUnit interface [COM]","GetParentState method","IOleParentUndoUnit.GetParentState","IOleParentUndoUnit::GetParentState","_ole_ioleparentundounit_getparentstate","com.ioleparentundounit_getparentstate","ocidl/IOleParentUndoUnit::GetParentState"]
old-location: com\ioleparentundounit_getparentstate.htm
tech.root: com
ms.assetid: 23eb1768-b68a-4b97-94a4-eeb7b840dda8
ms.date: 12/05/2018
ms.keywords: GetParentState, GetParentState method [COM], GetParentState method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],GetParentState method, IOleParentUndoUnit.GetParentState, IOleParentUndoUnit::GetParentState, _ole_ioleparentundounit_getparentstate, com.ioleparentundounit_getparentstate, ocidl/IOleParentUndoUnit::GetParentState
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
 - IOleParentUndoUnit::GetParentState
 - ocidl/IOleParentUndoUnit::GetParentState
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
 - IOleParentUndoUnit.GetParentState
---

# IOleParentUndoUnit::GetParentState


## -description

Retrieves state information about the innermost open parent undo unit.

## -parameters

### -param pdwState [out]

A pointer to the state information. This information is a value taken from the <a href="/windows/desktop/api/ocidl/ne-ocidl-uasflags">UASFLAGS</a> enumeration.

## -returns

This method returns S_OK on success.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the unit has an open child, it should delegate this method to that child. If not, it should fill in <i>pdwState</i> values appropriately and return. Note that a parent unit must never be blocked while it has an open child. If this happened it could prevent the child unit from being closed, which would cause serious problems.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When checking for a normal state, use the UAS_MASK value to mask unused bits in the <i>pdwState</i> parameter to this method for future compatibility.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>
