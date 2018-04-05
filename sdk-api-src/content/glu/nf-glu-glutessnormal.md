---
UID: NF:glu.gluTessNormal
title: gluTessNormal function
author: windows-driver-content
description: The gluTessNormal function specifies a normal for a polygon.
old-location: opengl\glutessnormal.htm
old-project: OpenGL
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluTessNormal, glu/gluTessNormal, gluTessNormal, gluTessNormal function [OpenGL], opengl.glutessnormal"
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
-	glu32.dll
api_name:
-	gluTessNormal
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessNormal function


## -description


The <b>gluTessNormal</b> function specifies a normal for a polygon.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param x

The x-coordinate component of a normal.


### -param y

The y-coordinate component of a normal.


### -param z

The z-coordinate component of a normal.


## -returns



This function does not return a value.




## -remarks



The <b>gluTessNormal</b> function describes a normal for a polygon that you define. All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal. (To obtain clockwise orientation, reverse the sign of the supplied normal). For example, if you know that all polygons lie in the x-y plane, call <b>gluTessNormal</b>(tess, 0.0, 0.0, 1.0) before rendering any polygons.

If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:

<ol>
<li>The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected. It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</li>
<li>The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</li>
</ol>
The supplied normal persists until another call to <b>gluTessNormal</b> changes it.




## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/c9ae2075-59d7-4c1a-b720-0aa05954525c">gluTessEndPolygon</a>
 

 

