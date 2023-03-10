---
UID: NE:ocidl.tagExtentMode
title: DVEXTENTMODE (ocidl.h)
description: Indicates whether the sizing mode is content or integral sizing.
helpviewer_keywords: ["DVEXTENTMODE","DVEXTENTMODE enumeration [COM]","DVEXTENT_CONTENT","DVEXTENT_INTEGRAL","_ole_DVEXTENTMODE","com.dvextentmode","ocidl/DVEXTENTMODE","ocidl/DVEXTENT_CONTENT","ocidl/DVEXTENT_INTEGRAL"]
old-location: com\dvextentmode.htm
tech.root: com
ms.assetid: 5848c26d-d185-4ad9-8841-bb8b622364ee
ms.date: 12/05/2018
ms.keywords: DVEXTENTMODE, DVEXTENTMODE enumeration [COM], DVEXTENT_CONTENT, DVEXTENT_INTEGRAL, _ole_DVEXTENTMODE, com.dvextentmode, ocidl/DVEXTENTMODE, ocidl/DVEXTENT_CONTENT, ocidl/DVEXTENT_INTEGRAL
req.header: ocidl.h
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
req.typenames: DVEXTENTMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagExtentMode
 - ocidl/tagExtentMode
 - DVEXTENTMODE
 - ocidl/DVEXTENTMODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - DVEXTENTMODE
---

# DVEXTENTMODE enumeration


## -description

Indicates whether the sizing mode is content or integral sizing.

## -enum-fields

### -field DVEXTENT_CONTENT:0

Indicates that the container will ask the object how big it wants to be to exactly fit its content, for example, in snap-to-size operations.

### -field DVEXTENT_INTEGRAL

Indicates that the container will provide a proposed size to the object for its use in resizing.

## -see-also

<a href="/windows/win32/api/ocidl/ns-ocidl-dvextentinfo">DVEXTENTINFO</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getnaturalextent">IViewObjectEx::GetNaturalExtent</a>
