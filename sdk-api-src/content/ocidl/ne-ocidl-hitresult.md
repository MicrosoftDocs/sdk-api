---
UID: NE:ocidl.tagHITRESULT
title: HITRESULT (ocidl.h)
description: Indicates whether a location is within the image of an object.
helpviewer_keywords: ["HITRESULT","HITRESULT enumeration [COM]","HITRESULT_CLOSE","HITRESULT_HIT","HITRESULT_OUTSIDE","HITRESULT_TRANSPARENT","_ole_HITRESULT","com.hitresult","ocidl/HITRESULT","ocidl/HITRESULT_CLOSE","ocidl/HITRESULT_HIT","ocidl/HITRESULT_OUTSIDE","ocidl/HITRESULT_TRANSPARENT"]
old-location: com\hitresult.htm
tech.root: com
ms.assetid: 44b070e4-5453-446c-a871-d977a8df8140
ms.date: 12/05/2018
ms.keywords: HITRESULT, HITRESULT enumeration [COM], HITRESULT_CLOSE, HITRESULT_HIT, HITRESULT_OUTSIDE, HITRESULT_TRANSPARENT, _ole_HITRESULT, com.hitresult, ocidl/HITRESULT, ocidl/HITRESULT_CLOSE, ocidl/HITRESULT_HIT, ocidl/HITRESULT_OUTSIDE, ocidl/HITRESULT_TRANSPARENT
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
req.typenames: HITRESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHITRESULT
 - ocidl/tagHITRESULT
 - HITRESULT
 - ocidl/HITRESULT
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
 - HITRESULT
---

# HITRESULT enumeration


## -description

Indicates whether a location is within the image of an object.

## -enum-fields

### -field HITRESULT_OUTSIDE:0

The specified location is outside the object and not close to the object.

### -field HITRESULT_TRANSPARENT:1

The specified location is within the bounds of the object, but not close to the image. For example, a point in the middle of a transparent circle could be HITRESULT_TRANSPARENT.

### -field HITRESULT_CLOSE:2

The specified location is inside the object or is outside the object but is close enough to the object to be considered inside. Small, thin or detailed objects may use this value. Even if a point is outside the bounding rectangle of an object it may still be close. This value is needed for hitting small objects.

### -field HITRESULT_HIT:3

The specified location is within the image of the object.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-queryhitpoint">IViewObjectEx::QueryHitPoint</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-queryhitrect">IViewObjectEx::QueryHitRect</a>
