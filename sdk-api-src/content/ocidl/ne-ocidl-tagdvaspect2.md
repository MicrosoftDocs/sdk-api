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

# tagDVASPECT2 enumeration


## -description


Specifies new drawing aspects used to optimize the drawing process.


## -enum-fields




### -field DVASPECT_OPAQUE

Represents the opaque, easy to clip parts of an object. Objects may or may not support this aspect.


### -field DVASPECT_TRANSPARENT

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
 

The container can determine which of these drawing aspects an object supports by calling the new method <a href="https://msdn.microsoft.com/cf8ec90c-07bb-4f60-93c9-4cee3fb5a056">IViewObjectEx::GetViewStatus</a>. Individual bits return information about which aspects are supported. If an object does not support the <a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a>interface, it is assumed to support only DVASPECT_CONTENT.

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




<a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>
 

 

