---
UID: NE:wtypes.tagSTGMOVE
title: STGMOVE (wtypes.h)
description: Indicate whether a storage element is to be moved or copied.
helpviewer_keywords: ["STGMOVE","STGMOVE enumeration [Structured Storage]","STGMOVE_COPY","STGMOVE_MOVE","STGMOVE_SHALLOWCOPY","_stg_stgmove","stg.stgmove","wtypes/STGMOVE","wtypes/STGMOVE_COPY","wtypes/STGMOVE_MOVE","wtypes/STGMOVE_SHALLOWCOPY"]
old-location: stg\stgmove.htm
tech.root: Stg
ms.assetid: f55c376b-f150-406a-b960-f096c2deeff1
ms.date: 12/05/2018
ms.keywords: STGMOVE, STGMOVE enumeration [Structured Storage], STGMOVE_COPY, STGMOVE_MOVE, STGMOVE_SHALLOWCOPY, _stg_stgmove, stg.stgmove, wtypes/STGMOVE, wtypes/STGMOVE_COPY, wtypes/STGMOVE_MOVE, wtypes/STGMOVE_SHALLOWCOPY
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STGMOVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTGMOVE
 - wtypes/tagSTGMOVE
 - STGMOVE
 - wtypes/STGMOVE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - STGMOVE
---

# STGMOVE enumeration


## -description

The 
<b>STGMOVE</b> enumeration values indicate whether a storage element is to be moved or copied. They are used in the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-moveelementto">IStorage::MoveElementTo</a> method.

## -enum-fields

### -field STGMOVE_MOVE:0

Indicates that the method should move the data from the source to the destination.

### -field STGMOVE_COPY:1

Indicates that the method should copy the data from the source to the destination. A copy is the same as a move except that the source element is not removed after copying the element to the destination. Copying an element on top of itself is undefined.

### -field STGMOVE_SHALLOWCOPY:2

Not implemented.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-moveelementto">IStorage::MoveElementTo</a>
