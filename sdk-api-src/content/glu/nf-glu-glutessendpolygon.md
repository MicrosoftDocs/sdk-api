---
UID: NF:glu.gluTessEndPolygon
title: gluTessEndPolygon function
author: windows-driver-content
description: The gluTessBeginPolygon and gluTessEndPolygon functions delimit a polygon description.
old-location: opengl\glutessendpolygon.htm
old-project: OpenGL
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluTessEndPolygon, gluTessEndPolygon, gluTessEndPolygon function [OpenGL], opengl.glutessendpolygon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: glu.h
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
-	Glu32.dll
api_name:
-	gluTessEndPolygon
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessEndPolygon function


## -description


The <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a> and <b>gluTessEndPolygon</b> functions delimit a polygon description.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a> and <b>gluTessEndPolygon</b> functions delimit the definition of a nonconvex polygon. Within each <b>gluTessBeginPolygon</b> / <b>gluTessEndPolygon</b> pair, include one or more calls to <a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>. Within each contour, there are zero or more calls to <a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>. The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).

The <i>polygon_data</i> parameter is a pointer to a programmer-defined data structure. If the appropriate callbacks are specified (see <a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.

When you call <b>gluTessEndPolygon</b>, the polygon is tessellated, and the resulting triangles are described through callbacks. For descriptions of the callback functions, see <a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>.


#### Examples

The following describes a quadrilateral with a triangular hole:

<pre class="syntax" xml:space="preserve"><code>gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>



<a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a>



<a href="https://msdn.microsoft.com/8c3a90d3-760d-4a0a-9808-a797383fcc42">gluTessNormal</a>



<a href="https://msdn.microsoft.com/1306b9ef-4f1e-4684-99ea-464bae1d0a61">gluTessProperty</a>



<a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>
 

 

