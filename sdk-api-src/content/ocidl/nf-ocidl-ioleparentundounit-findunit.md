---
UID: NF:ocidl.IOleParentUndoUnit.FindUnit
title: IOleParentUndoUnit::FindUnit (ocidl.h)
description: Indicates whether the specified unit is a child of this undo unit or one of its children, that is if the specified unit is part of the hierarchy in this parent unit.
helpviewer_keywords: ["FindUnit","FindUnit method [COM]","FindUnit method [COM]","IOleParentUndoUnit interface","IOleParentUndoUnit interface [COM]","FindUnit method","IOleParentUndoUnit.FindUnit","IOleParentUndoUnit::FindUnit","_ole_ioleparentundounit_findunit","com.ioleparentundounit_findunit","ocidl/IOleParentUndoUnit::FindUnit"]
old-location: com\ioleparentundounit_findunit.htm
tech.root: com
ms.assetid: 096e6cc4-7843-49fa-b1d7-bce034d4b7ce
ms.date: 12/05/2018
ms.keywords: FindUnit, FindUnit method [COM], FindUnit method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],FindUnit method, IOleParentUndoUnit.FindUnit, IOleParentUndoUnit::FindUnit, _ole_ioleparentundounit_findunit, com.ioleparentundounit_findunit, ocidl/IOleParentUndoUnit::FindUnit
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
 - IOleParentUndoUnit::FindUnit
 - ocidl/IOleParentUndoUnit::FindUnit
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
 - IOleParentUndoUnit.FindUnit
---

# IOleParentUndoUnit::FindUnit


## -description

Indicates whether the specified unit is a child of this undo unit or one of its children, that is if the specified unit is part of the hierarchy in this parent unit.

## -parameters

### -param pUU [in]

 An <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a> pointer to the undo unit to be found.

## -returns

This method returns S_OK if the specified undo unit is in the hierarchy subordinate to this parent; otherwise, S_FALSE.

## -remarks

This is typically called by the undo manager in its implementation of its <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-discardfrom">IOleUndoManager::DiscardFrom</a> method in the rare event that the unit being discarded is not a top-level unit. The parent unit should look in its own list first, then delegate to each child that is also a parent unit, as determined by doing a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> for <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-discardfrom">IOleUndoManager::DiscardFrom</a>