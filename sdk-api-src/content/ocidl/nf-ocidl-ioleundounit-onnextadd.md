---
UID: NF:ocidl.IOleUndoUnit.OnNextAdd
title: IOleUndoUnit::OnNextAdd (ocidl.h)
description: Notifies the last undo unit in the collection that a new unit has been added.
helpviewer_keywords: ["IOleUndoUnit interface [COM]","OnNextAdd method","IOleUndoUnit.OnNextAdd","IOleUndoUnit::OnNextAdd","OnNextAdd","OnNextAdd method [COM]","OnNextAdd method [COM]","IOleUndoUnit interface","_ole_ioleundounit_onnextadd","com.ioleundounit_onnextadd","ocidl/IOleUndoUnit::OnNextAdd"]
old-location: com\ioleundounit_onnextadd.htm
tech.root: com
ms.assetid: 79bbdb6c-cae3-4f9a-b335-565aacec6d3e
ms.date: 12/05/2018
ms.keywords: IOleUndoUnit interface [COM],OnNextAdd method, IOleUndoUnit.OnNextAdd, IOleUndoUnit::OnNextAdd, OnNextAdd, OnNextAdd method [COM], OnNextAdd method [COM],IOleUndoUnit interface, _ole_ioleundounit_onnextadd, com.ioleundounit_onnextadd, ocidl/IOleUndoUnit::OnNextAdd
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
 - IOleUndoUnit::OnNextAdd
 - ocidl/IOleUndoUnit::OnNextAdd
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
 - IOleUndoUnit.OnNextAdd
---

# IOleUndoUnit::OnNextAdd


## -description

Notifies the last undo unit in the collection that a new unit has been added.



## -returns

Implementations of this method always return S_OK. The <b>HRESULT</b> return type is used only for remotability.

## -remarks

An object can create an undo unit for an action and add it to the undo manager but can continue inserting data into it through private interfaces. When the undo unit receives a call to this method, it communicates back to the creating object that the context has changed. Then, the creating object stops inserting data into the undo unit.

The parent undo unit calls this method on its most recently added child undo unit to notify the child unit that the context has changed and a new undo unit has been added.

For example, this method is used for supporting fuzzy actions, like typing, which do not have a clear point of termination but instead are terminated only when something else happens.

This method may not always be called if the undo manager or an open parent unit chooses to discard the unit by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> instead. Any connection which feeds data to the undo unit behind the scenes through private interfaces should not <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> the undo unit.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Note that parent units merely delegate this method to their most recently added child unit. A parent unit should terminate communication through any private interfaces when it is closed. A parent unit knows it is being closed when it receives S_FALSE from calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>
