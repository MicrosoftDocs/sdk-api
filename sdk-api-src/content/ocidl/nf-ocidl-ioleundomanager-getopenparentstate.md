---
UID: NF:ocidl.IOleUndoManager.GetOpenParentState
title: IOleUndoManager::GetOpenParentState (ocidl.h)
description: Retrieves state information about the innermost open parent undo unit. (IOleUndoManager.GetOpenParentState)
helpviewer_keywords: ["GetOpenParentState","GetOpenParentState method [COM]","GetOpenParentState method [COM]","IOleUndoManager interface","IOleUndoManager interface [COM]","GetOpenParentState method","IOleUndoManager.GetOpenParentState","IOleUndoManager::GetOpenParentState","_ole_ioleundomanager_getopenparentstate","com.ioleundomanager_getopenparentstate","ocidl/IOleUndoManager::GetOpenParentState"]
old-location: com\ioleundomanager_getopenparentstate.htm
tech.root: com
ms.assetid: 32a4e08a-409b-4f0e-8374-1cdf3b558928
ms.date: 12/05/2018
ms.keywords: GetOpenParentState, GetOpenParentState method [COM], GetOpenParentState method [COM],IOleUndoManager interface, IOleUndoManager interface [COM],GetOpenParentState method, IOleUndoManager.GetOpenParentState, IOleUndoManager::GetOpenParentState, _ole_ioleundomanager_getopenparentstate, com.ioleundomanager_getopenparentstate, ocidl/IOleUndoManager::GetOpenParentState
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
 - IOleUndoManager::GetOpenParentState
 - ocidl/IOleUndoManager::GetOpenParentState
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
 - IOleUndoManager.GetOpenParentState
---

# IOleUndoManager::GetOpenParentState


## -description

Retrieves state information about the innermost open parent undo unit.

## -parameters

### -param pdwState [out]

A pointer to a variable that receives the state information. This information is a value taken from the <a href="/windows/desktop/api/ocidl/ne-ocidl-uasflags">UASFLAGS</a> enumeration.

## -returns

This method returns S_OK if there is an open parent unit and its state was successfully returned or the undo manager is disabled; otherwise, S_FALSE.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When checking for a normal state, use the UAS_MASK value to mask unused bits in the <i>pdwState</i> parameter to this method for future compatibility. 


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If there is an open parent unit, this method calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-getparentstate">IOleParentUndoUnit::GetParentState</a>.

If the undo manager is disabled, it should fill the <i>pdwState</i> parameter with UAS_BLOCKED and return S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-uasflags">UASFLAGS</a>
