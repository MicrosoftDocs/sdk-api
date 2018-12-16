---
UID: NE:ocidl.tagVIEWSTATUS
title: VIEWSTATUS
author: windows-sdk-content
description: Specifies the opacity of the object and the drawing aspects supported by the object.
old-location: com\viewstatus.htm
tech.root: com
ms.assetid: 7b3118af-db29-4eb1-9b1b-38a8ebe42f19
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VIEWSTATUS, VIEWSTATUS enumeration [COM], VIEWSTATUS_3DSURFACE, VIEWSTATUS_DVASPECTOPAQUE, VIEWSTATUS_DVASPECTTRANSPARENT, VIEWSTATUS_OPAQUE, VIEWSTATUS_SOLIDBKGND, VIEWSTATUS_SURFACE, _ole_VIEWSTATUS, com.viewstatus, ocidl/VIEWSTATUS, ocidl/VIEWSTATUS_3DSURFACE, ocidl/VIEWSTATUS_DVASPECTOPAQUE, ocidl/VIEWSTATUS_DVASPECTTRANSPARENT, ocidl/VIEWSTATUS_OPAQUE, ocidl/VIEWSTATUS_SOLIDBKGND, ocidl/VIEWSTATUS_SURFACE
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - VIEWSTATUS
product: Windows
targetos: Windows
req.typenames: VIEWSTATUS
req.redist: 
---

# VIEWSTATUS enumeration


## -description


Specifies the opacity of the object and the drawing aspects supported by the object.




## -enum-fields




### -field VIEWSTATUS_OPAQUE

The object is completely opaque. So, for any aspect, it promises to draw the entire rectangle passed to the <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method. If this value is not set, the object contains transparent parts. If it also support DVASPECT_TRANSPARENT, then this aspect may be used to draw the transparent parts only.

This bit applies only to CONTENT related aspects and not to DVASPECT_ICON or DVASPECT_DOCPRINT. 


### -field VIEWSTATUS_SOLIDBKGND

The object has a solid background (consisting in a solid color, not a brush pattern). This bit is meaningful only if VIEWSTATUS_OPAQUE is set.

This bit applies only to CONTENT related aspects and not to DVASPECT_ICON or DVASPECT_DOCPRINT. 


### -field VIEWSTATUS_DVASPECTOPAQUE

The object supports DVASPECT_OPAQUE. All <a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a> methods taking a drawing aspect as a parameter can be called with this aspect.


### -field VIEWSTATUS_DVASPECTTRANSPARENT

The object supports DVASPECT_TRANSPARENT. All <a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a> methods taking a drawing aspect as a parameter can be called with this aspect.



### -field VIEWSTATUS_SURFACE

The object supports a 2-dimensional surface.


### -field VIEWSTATUS_3DSURFACE

The object supports a 3-dimensional surface.


## -see-also




<a href="https://msdn.microsoft.com/cf8ec90c-07bb-4f60-93c9-4cee3fb5a056">IViewObjectEx::GetViewStatus</a>
 

 

