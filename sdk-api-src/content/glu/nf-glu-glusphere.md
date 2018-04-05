---
UID: NF:glu.gluSphere
title: gluSphere function
author: windows-driver-content
description: The gluSphere function draws a sphere.
old-location: opengl\glusphere.htm
old-project: OpenGL
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluSphere, glu/gluSphere, gluSphere, gluSphere function [OpenGL], opengl.glusphere"
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
-	gluSphere
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluSphere function


## -description


The <b>gluSphere</b> function draws a sphere.


## -parameters




### -param qobj

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param radius

The radius of the sphere.


### -param slices

The number of subdivisions around the z-axis (similar to lines of longitude).


### -param stacks

The number of subdivisions along the z-axis (similar to lines of latitude).


## -returns



This function does not return a value.




## -remarks



The <b>gluSphere</b> function draws a sphere of the given radius centered around the origin. The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).

If the orientation is set to GLU_OUTSIDE (with <b>gluQuadricOrientation</b>), any normals generated point away from the center of the sphere. Otherwise, they point toward the center of the sphere.

If texturing is turned on (with <b>gluQuadricTexture</b>): texture coordinates are generated so that <i>t</i> ranges from 0.0 at <i>z</i> = -<i>radius</i> to 1.0 at <i>z</i> = <i>radius</i> (<i>t</i> increases linearly along longitudinal lines); and <i>s</i> ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.




## -see-also




<a href="https://msdn.microsoft.com/43329d2f-50bb-46ea-85cb-22956d0df375">gluCylinder</a>



<a href="https://msdn.microsoft.com/c9260621-930d-47dd-a046-30895779473b">gluDisk</a>



<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/46809c15-88c3-40fa-965a-7aeeedc1c598">gluPartialDisk</a>



<a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>
 

 

