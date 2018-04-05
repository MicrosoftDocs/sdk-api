---
UID: NF:gl.glRectf
title: glRectf function
author: windows-driver-content
description: The glRectf function draws a rectangle.
old-location: opengl\glrectf.htm
old-project: OpenGL
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glRectf, glRectf, glRectf function [OpenGL], opengl.glrectf
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
-	glRectf
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glRectf function


## -description


The <a href="https://msdn.microsoft.com/d5574c22-7ae1-4040-9b95-769693fa41e3">glRectf</a> function draws a rectangle.


## -parameters




### -param x1

The <i>x</i> coordinate of the vertex of a rectangle.


### -param y1

The <i>y</i> coordinate of the vertex of a rectangle.


### -param x2

The <i>x</i> coordinate of the opposite vertex of the rectangle.


### -param y2

The <i>y</i> coordinate of the opposite vertex of the rectangle.


## -returns



This function does not return a value.




## -remarks



The <b>glRectf</b> function supports efficient specification of rectangles as two corner points. Each rectangle command takes four arguments, organized either as two consecutive pairs of (<i>x</i>, <i>y</i>) coordinates, or as two pointers to arrays, each containing an (<i>x</i>, <i>y</i>) pair. The resulting rectangle is defined in the <i>z</i> = 0 plane.


The <b>glRectf</b>(<i>x1,</i> <i>y1,</i> <i>x2,</i> <i>y2</i>) function is exactly equivalent to the following sequence:


<b>glBegin</b>(GL_POLYGON);

<b>glVertex2</b>(
        <i>x1,</i> <i>y1</i>
        );

<b>glVertex2</b>(
        <i>x2,</i> <i>y1</i>
        );

<b>glVertex2</b>(
        <i>x2,</i> <i>y2</i>
        );

<b>glVertex2</b>(
        <i>x1,</i> <i>y2</i>
        );

<b>glEnd</b>( );

Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

