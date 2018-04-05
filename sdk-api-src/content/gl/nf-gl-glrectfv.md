---
UID: NF:gl.glRectfv
title: glRectfv function
author: windows-driver-content
description: The glRectfv function draws a rectangle.
old-location: opengl\glrectfv.htm
old-project: OpenGL
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glRectfv, glRectfv, glRectfv function [OpenGL], opengl.glrectfv
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
-	glRectfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glRectfv function


## -description


The <a href="https://msdn.microsoft.com/53000734-bfc3-42c3-aa80-0a54e3dd36ec">glRectfv</a> function draws a rectangle.


## -parameters




### -param v1

A pointer to one vertex of a rectangle.


### -param v2

a pointer to the opposite vertex of the rectangle.


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
 

 

