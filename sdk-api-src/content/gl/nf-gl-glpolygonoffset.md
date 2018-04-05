---
UID: NF:gl.glPolygonOffset
title: glPolygonOffset function
author: windows-driver-content
description: The glPolygonOffset function sets the scale and units OpenGL uses to calculate depth values.
old-location: opengl\glpolygonoffset.htm
old-project: OpenGL
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glPolygonOffset, gl/glPolygonOffset, glPolygonOffset, glPolygonOffset function [OpenGL], opengl.glpolygonoffset"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	glPolygonOffset
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPolygonOffset function


## -description


The <b>glPolygonOffset</b> function sets the scale and units OpenGL uses to calculate depth values.


## -parameters




### -param factor

Specifies a scale factor that is used to create a variable depth offset for each polygon. The initial value is zero.


### -param units

Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset. The initial value is 0.


## -returns



This function does not return a value.




## -remarks



When GL_POLYGON_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices. The value of the offset is <i>factor</i> * Δz + r *<i>units</i>, where Δz is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation. The offset is added before the depth test is performed and before the value is written into the depth buffer.

The <b>glPolygonOffset</b> function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.

The <b>glPolygonOffset</b> function has no effect on depth coordinates placed in the feedback buffer. It also has no effect on selection.
        
        
        

The following functions retrieve information related to <b>glPolygonOffset</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_POLYGON_OFFSET_FACTOR</li>
<li>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_POLYGON_OFFSET_UNITS</li>
<li>
<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_POLYGON_OFFSET_FILL</li>
<li>
<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_POLYGON_OFFSET_LINE</li>
<li>
<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_POLYGON_OFFSET_POINT</li>
</ul>
<div class="alert"><b>Note</b>  The <b>glPolygonOffset</b> function is only available in OpenGl version 1.1 or greater.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>
 

 

