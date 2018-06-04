---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagVIEWSTATUS enumeration


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
 

 

