---
UID: NF:glu.gluCylinder
title: gluCylinder function
author: windows-driver-content
description: The gluCylinder function draws a cylinder.
old-location: opengl\glucylinder.htm
old-project: OpenGL
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluCylinder, glu/gluCylinder, gluCylinder, gluCylinder function [OpenGL], opengl.glucylinder"
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
-	gluCylinder
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluCylinder function


## -description


The <b>gluCylinder</b> function draws a cylinder.


## -parameters




### -param qobj

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param baseRadius

The radius of the cylinder at <i>z</i> = 0.


### -param topRadius

The radius of the cylinder at <i>z</i> = <i>height</i>.


### -param height

The height of the cylinder.


### -param slices

The number of subdivisions around the z-axis.


### -param stacks

The number of subdivisions along the z-axis.


## -returns



This function does not return a value.




## -remarks



The <b>gluCylinder</b> function draws a cylinder oriented along the z-axis. The base of the cylinder is placed at <i>z</i> = 0, and the top at <i>z</i> = <i>height</i>. Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.

Note that if <i>topRadius</i> is set to zero, then this routine will generate a cone.

If the orientation is set to GLU_OUTSIDE (with <a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>), then any generated normals point away from the z-axis. Otherwise, they point toward the z-axis.

If texturing is turned on (with <a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>): texture coordinates are generated so that <i>t</i> ranges linearly from 0.0 at <i>z</i> = 0 to 1.0 at <i>z</i> = <i>height</i>; and <i>s</i> ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.




## -see-also




<a href="https://msdn.microsoft.com/c9260621-930d-47dd-a046-30895779473b">gluDisk</a>



<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/46809c15-88c3-40fa-965a-7aeeedc1c598">gluPartialDisk</a>



<a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>



<a href="https://msdn.microsoft.com/0f1919c6-0551-4d50-b782-767dacc088cb">gluSphere</a>
 

 

