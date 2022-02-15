---
UID: NE:ocidl.tagVIEWSTATUS
title: VIEWSTATUS (ocidl.h)
description: Specifies the opacity of the object and the drawing aspects supported by the object.
helpviewer_keywords: ["VIEWSTATUS","VIEWSTATUS enumeration [COM]","VIEWSTATUS_3DSURFACE","VIEWSTATUS_DVASPECTOPAQUE","VIEWSTATUS_DVASPECTTRANSPARENT","VIEWSTATUS_OPAQUE","VIEWSTATUS_SOLIDBKGND","VIEWSTATUS_SURFACE","_ole_VIEWSTATUS","com.viewstatus","ocidl/VIEWSTATUS","ocidl/VIEWSTATUS_3DSURFACE","ocidl/VIEWSTATUS_DVASPECTOPAQUE","ocidl/VIEWSTATUS_DVASPECTTRANSPARENT","ocidl/VIEWSTATUS_OPAQUE","ocidl/VIEWSTATUS_SOLIDBKGND","ocidl/VIEWSTATUS_SURFACE"]
old-location: com\viewstatus.htm
tech.root: com
ms.assetid: 7b3118af-db29-4eb1-9b1b-38a8ebe42f19
ms.date: 12/05/2018
ms.keywords: VIEWSTATUS, VIEWSTATUS enumeration [COM], VIEWSTATUS_3DSURFACE, VIEWSTATUS_DVASPECTOPAQUE, VIEWSTATUS_DVASPECTTRANSPARENT, VIEWSTATUS_OPAQUE, VIEWSTATUS_SOLIDBKGND, VIEWSTATUS_SURFACE, _ole_VIEWSTATUS, com.viewstatus, ocidl/VIEWSTATUS, ocidl/VIEWSTATUS_3DSURFACE, ocidl/VIEWSTATUS_DVASPECTOPAQUE, ocidl/VIEWSTATUS_DVASPECTTRANSPARENT, ocidl/VIEWSTATUS_OPAQUE, ocidl/VIEWSTATUS_SOLIDBKGND, ocidl/VIEWSTATUS_SURFACE
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
req.typenames: VIEWSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVIEWSTATUS
 - ocidl/tagVIEWSTATUS
 - VIEWSTATUS
 - ocidl/VIEWSTATUS
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
 - VIEWSTATUS
---

# VIEWSTATUS enumeration


## -description

Specifies the opacity of the object and the drawing aspects supported by the object.

## -enum-fields

### -field VIEWSTATUS_OPAQUE:1

The object is completely opaque. So, for any aspect, it promises to draw the entire rectangle passed to the <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method. If this value is not set, the object contains transparent parts. If it also support DVASPECT_TRANSPARENT, then this aspect may be used to draw the transparent parts only.

This bit applies only to CONTENT related aspects and not to DVASPECT_ICON or DVASPECT_DOCPRINT.

### -field VIEWSTATUS_SOLIDBKGND:2

The object has a solid background (consisting in a solid color, not a brush pattern). This bit is meaningful only if VIEWSTATUS_OPAQUE is set.

This bit applies only to CONTENT related aspects and not to DVASPECT_ICON or DVASPECT_DOCPRINT.

### -field VIEWSTATUS_DVASPECTOPAQUE:4

The object supports DVASPECT_OPAQUE. All <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> methods taking a drawing aspect as a parameter can be called with this aspect.

### -field VIEWSTATUS_DVASPECTTRANSPARENT:8

The object supports DVASPECT_TRANSPARENT. All <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> methods taking a drawing aspect as a parameter can be called with this aspect.

### -field VIEWSTATUS_SURFACE:16

The object supports a 2-dimensional surface.

### -field VIEWSTATUS_3DSURFACE:32

The object supports a 3-dimensional surface.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getviewstatus">IViewObjectEx::GetViewStatus</a>
