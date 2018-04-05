---
UID: NF:glu.gluDisk
title: gluDisk function
author: windows-driver-content
description: The gluDisk function draws a disk.
old-location: opengl\gludisk.htm
old-project: OpenGL
ms.assetid: c9260621-930d-47dd-a046-30895779473b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluDisk, glu/gluDisk, gluDisk, gluDisk function [OpenGL], opengl.gludisk"
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
-	gluDisk
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluDisk function


## -description


The <b>gluDisk</b> function draws a disk.


## -parameters




### -param qobj

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param innerRadius

The inner radius of the disk (may be zero).


### -param outerRadius

The outer radius of the disk.


### -param slices

The number of subdivisions around the z-axis.


### -param loops

The number of concentric rings about the origin into which the disk is subdivided.


## -returns



This function does not return a value.




## -remarks



The <b>gluDisk</b> function renders a disk on the <i>z</i> = 0 plane. The disk has a radius of <i>outerRadius</i>, and contains a concentric circular hole with a radius of <i>innerRadius</i>. If <i>innerRadius</i> is 0, then no hole is generated. The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by <i>slices</i> and <i>loops</i>, respectively).

With respect to orientation, the positive <i>z</i>-side of the disk is considered to be <i>outside</i> (see <a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>). This means that if the orientation is set to GLU_OUTSIDE, then any normals generated point along the positive z-axis.

If texturing is turned on (with <a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>), texture coordinates are generated linearly such that where <i>r</i> = <i>outerRadius</i>, the value at (<i>r</i>, 0, 0) is (1, 0.5); at (0, <i>r</i>, 0) it is (0.5, 1); at (-<i>r</i>, 0, 0) it is (0, 0.5); and at (0, -<i>r</i>, 0) it is (0.5, 0).




## -see-also




<a href="https://msdn.microsoft.com/43329d2f-50bb-46ea-85cb-22956d0df375">gluCylinder</a>



<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/46809c15-88c3-40fa-965a-7aeeedc1c598">gluPartialDisk</a>



<a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>



<a href="https://msdn.microsoft.com/0f1919c6-0551-4d50-b782-767dacc088cb">gluSphere</a>
 

 

