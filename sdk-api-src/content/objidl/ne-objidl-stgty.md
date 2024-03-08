---
UID: NE:objidl.tagSTGTY
title: STGTY (objidl.h)
description: The STGTY enumeration values are used in the type member of the STATSTG structure to indicate the type of the storage element. A storage element is a storage object, a stream object, or a byte-array object (LOCKBYTES).
helpviewer_keywords: ["STGTY","STGTY enumeration [Structured Storage]","STGTY_LOCKBYTES","STGTY_PROPERTY","STGTY_STORAGE","STGTY_STREAM","_stg_stgty","objidl/STGTY","objidl/STGTY_LOCKBYTES","objidl/STGTY_PROPERTY","objidl/STGTY_STORAGE","objidl/STGTY_STREAM","stg.stgty"]
old-location: stg\stgty.htm
tech.root: Stg
ms.assetid: 67189e7a-b089-4a29-adf8-ad7c459c7974
ms.date: 12/05/2018
ms.keywords: STGTY, STGTY enumeration [Structured Storage], STGTY_LOCKBYTES, STGTY_PROPERTY, STGTY_STORAGE, STGTY_STREAM, _stg_stgty, objidl/STGTY, objidl/STGTY_LOCKBYTES, objidl/STGTY_PROPERTY, objidl/STGTY_STORAGE, objidl/STGTY_STREAM, stg.stgty
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STGTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTGTY
 - objidl/tagSTGTY
 - STGTY
 - objidl/STGTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - STGTY
---

# STGTY enumeration


## -description

The 
<b>STGTY</b> enumeration values are used in the <b>type</b> member of the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure to indicate the type of the storage element. A storage element is a storage object, a stream object, or a byte-array object (LOCKBYTES).

## -enum-fields

### -field STGTY_STORAGE:1

Indicates that the storage element is a storage object.

### -field STGTY_STREAM:2

Indicates that the storage element is a stream object.

### -field STGTY_LOCKBYTES:3

Indicates that the storage element is a byte-array object.

### -field STGTY_PROPERTY:4

Indicates that the storage element is a property storage object.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
