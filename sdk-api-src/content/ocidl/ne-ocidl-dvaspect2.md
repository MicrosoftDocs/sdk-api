---
UID: NE:ocidl.tagDVASPECT2
title: DVASPECT2 (ocidl.h)
description: Specifies new drawing aspects used to optimize the drawing process.
helpviewer_keywords: ["DVASPECT2","DVASPECT2 enumeration [COM]","DVASPECT_OPAQUE","DVASPECT_TRANSPARENT","_ole_DVASPECT2","com.dvaspect2","ocidl/DVASPECT2","ocidl/DVASPECT_OPAQUE","ocidl/DVASPECT_TRANSPARENT"]
old-location: com\dvaspect2.htm
tech.root: com
ms.assetid: 9000b807-5a42-437f-a3e8-a7b23be1665b
ms.date: 12/05/2018
ms.keywords: DVASPECT2, DVASPECT2 enumeration [COM], DVASPECT_OPAQUE, DVASPECT_TRANSPARENT, _ole_DVASPECT2, com.dvaspect2, ocidl/DVASPECT2, ocidl/DVASPECT_OPAQUE, ocidl/DVASPECT_TRANSPARENT
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
req.typenames: DVASPECT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVASPECT2
 - ocidl/tagDVASPECT2
 - DVASPECT2
 - ocidl/DVASPECT2
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
 - DVASPECT2
---

# DVASPECT2 enumeration


## -description

Specifies new drawing aspects used to optimize the drawing process.

## -enum-fields

### -field DVASPECT_OPAQUE:16

Represents the opaque, easy to clip parts of an object. Objects may or may not support this aspect.

### -field DVASPECT_TRANSPARENT:32

Represents the transparent or irregular parts of on object, typically parts that are expensive or impossible to clip out. Objects may or may not support this aspect.

## -remarks

To support drawing optimizations to reduce flicker, an object needs to be able to draw and return information about three separate aspects of itself.

<table>
<tr>
<th>Aspect</th>
<th>Description</th>
</tr>
<tr>
<td>
DVASPECT_CONTENT

</td>
<td>
Specifies the entire content of an object. All objects should support this aspect.

</td>
</tr>
<tr>
<td>
DVASPECT_OPAQUE

</td>
<td>
Represents the opaque, easy to clip parts of an object. Objects may or may not support this aspect.

</td>
</tr>
<tr>
<td>
DVASPECT_TRANSPARENT

</td>
<td>
Represents the transparent or irregular parts of on object, typically parts that are expensive or impossible to clip out. Objects may or may not support this aspect.

</td>
</tr>
</table>
 

The container can determine which of these drawing aspects an object supports by calling the new method <a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getviewstatus">IViewObjectEx::GetViewStatus</a>. Individual bits return information about which aspects are supported. If an object does not support the <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> interface, it is assumed to support only DVASPECT_CONTENT.

Depending on which aspects are supported, the container can ask the object to draw itself during the front to back pass only, the back to front pass only, or both. The various possible cases are: 



<ul>
<li>Objects supporting only DVASPECT_CONTENT should be drawn during the back to front pass, with all opaque parts of any overlapping object clipped out. Since all objects should support this aspect, a container not concerned about flickering - maybe because it is drawing in an offscreen bitmap - can opt to draw all objects that way and skip the front to back pass.
</li>
<li>Objects supporting DVASPECT_OPAQUE may be asked to draw this aspect during the front to back pass. The container is responsible for clipping out the object's opaque regions before painting any further object behind it.
</li>
<li>Objects supporting DVASPECT_TRANSPARENT may be asked to draw this aspect during the back to front pass. The container is responsible for clipping out opaque parts of overlapping objects before letting an object draw this aspect.
</li>
</ul>
Even when DVASPECT_OPAQUE and DVASPECT_TRANSPARENT are supported, the container is free to use these aspects or not. In particular, if it is painting in an offscreen bitmap and consequently is unconcerned about flicker, the container may use DVASPECT_CONTENT and a one-pass drawing only. However, in a two-pass drawing, if the container uses DVASPECT_OPAQUE during the front to back pass, then it must use DVASPECT_TRANSPARENT during the back to front pass to complete the rendering of the object.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>
