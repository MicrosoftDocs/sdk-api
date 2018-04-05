---
UID: NF:glu.gluPwlCurve
title: gluPwlCurve function
author: windows-driver-content
description: The gluPwlCurve function describes a piecewise linear Non-Uniform Rational B-Spline (NURBS) trimming curve.
old-location: opengl\glupwlcurve.htm
old-project: OpenGL
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluPwlCurve, glu/gluPwlCurve, gluPwlCurve, gluPwlCurve function [OpenGL], opengl.glupwlcurve"
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
-	gluPwlCurve
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluPwlCurve function


## -description


The <b>gluPwlCurve</b> function describes a piecewise linear Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) trimming curve.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param count

The number of points on the curve.


### -param array

An array containing the curve points.


### -param stride

The offset (a number of single-precision floating-point values) between points on the curve.


### -param type

The type of curve. Must be either GLU_MAP1_TRIM_2 or GLU_MAP1_TRIM_3.


## -returns



This function does not return a value.




## -remarks



The <b>gluPwlCurve</b> function describes a piecewise linear trimming curve for a NURBS surface. A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed. These points are connected with line segments to form a curve. If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.

If <i>type</i> is GLU_MAP1_TRIM_2, it describes a curve in two-dimensional (<i>u</i> and <i>v</i>) parameter space. If it is GLU_MAP1_TRIM_3, then it describes a curve in two-dimensional homogeneous (<i>u</i>, <i>v</i>, and <i>w</i>) parameter space. For more information about trimming curves, see <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f2e765-1a07-4faa-940c-9cb957dd54d4">gluBeginCurve</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>
 

 

