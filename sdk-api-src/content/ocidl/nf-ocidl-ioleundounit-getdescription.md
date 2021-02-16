---
UID: NF:ocidl.IOleUndoUnit.GetDescription
title: IOleUndoUnit::GetDescription (ocidl.h)
description: Retrieves a description of the undo unit that can be used in the undo or redo user interface.
helpviewer_keywords: ["GetDescription","GetDescription method [COM]","GetDescription method [COM]","IOleUndoUnit interface","IOleUndoUnit interface [COM]","GetDescription method","IOleUndoUnit.GetDescription","IOleUndoUnit::GetDescription","_ole_ioleundounit_getdescription","com.ioleundounit_getdescription","ocidl/IOleUndoUnit::GetDescription"]
old-location: com\ioleundounit_getdescription.htm
tech.root: com
ms.assetid: 8fd9c49c-a8f3-4a4a-b501-211a107c1305
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [COM], GetDescription method [COM],IOleUndoUnit interface, IOleUndoUnit interface [COM],GetDescription method, IOleUndoUnit.GetDescription, IOleUndoUnit::GetDescription, _ole_ioleundounit_getdescription, com.ioleundounit_getdescription, ocidl/IOleUndoUnit::GetDescription
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
 - IOleUndoUnit::GetDescription
 - ocidl/IOleUndoUnit::GetDescription
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
 - IOleUndoUnit.GetDescription
---

# IOleUndoUnit::GetDescription


## -description

Retrieves a description of the undo unit that can be used in the undo or redo user interface.

## -parameters

### -param pBstr [out]

A pointer to string that describes this undo unit.

## -returns

This method returns S_OK on success.

## -remarks

All units are required to provide a user-readable description of themselves.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <i>pbstr</i> parameter is allocated with the standard string allocator. The caller is responsible for freeing this string.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>