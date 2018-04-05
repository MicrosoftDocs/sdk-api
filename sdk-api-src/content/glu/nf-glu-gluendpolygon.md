---
UID: NF:glu.gluEndPolygon
title: gluEndPolygon function
author: windows-driver-content
description: The gluBeginPolygon and gluEndPolygon functions delimit a polygon description.
old-location: opengl\gluendpolygon.htm
old-project: OpenGL
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluEndPolygon, gluEndPolygon, gluEndPolygon function [OpenGL], opengl.gluendpolygon
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
-	gluEndPolygon
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluEndPolygon function


## -description


<p class="CCE_Message">[The <b>gluEndPolygon</b> function is obsolete and is provided for backward compatibility only. The <b>gluEndPolygon</b> function is mapped to <b>gluTessEndPolygon</b> followed by <b>gluTessEndContour</b>.]

The <a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluBeginPolygon</a> and <b>gluEndPolygon</b> functions delimit a polygon description.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


## -returns



This function does not return a value.




## -remarks



Use <a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluBeginPolygon</a> and <b>gluEndPolygon</b> to delimit the definition of a nonconvex polygon.

<ol>
<li>Call <b>gluBeginPolygon</b>.</li>
<li>Define the contours of the polygon by calling <a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a> for each vertex and <a href="https://msdn.microsoft.com/622cd631-3426-4206-9e23-af2a74343da5">gluNextContour</a> to start each new contour.</li>
<li>Call <b>gluEndPolygon</b> to signal the end of the definition.Once <b>gluEndPolygon</b> is called, the polygon is tessellated, and the resulting triangles are described through callbacks. For descriptions of the callback functions, see <a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>.

</li>
</ol>

#### Examples

The following example describes a quadrilateral with a triangular hole: 

<pre class="syntax" xml:space="preserve"><code>gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/622cd631-3426-4206-9e23-af2a74343da5">gluNextContour</a>



<a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>



<a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>



<a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>
 

 

