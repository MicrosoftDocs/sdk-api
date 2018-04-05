---
UID: NF:glu.gluNurbsCurve
title: gluNurbsCurve function
author: windows-driver-content
description: The gluNurbsCurve function defines the shape of a Non-Uniform Rational B-Spline (NURBS) curve.
old-location: opengl\glunurbscurve.htm
old-project: OpenGL
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluNurbsCurve, glu/gluNurbsCurve, gluNurbsCurve, gluNurbsCurve function [OpenGL], opengl.glunurbscurve"
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
-	gluNurbsCurve
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNurbsCurve function


## -description


The <b>gluNurbsCurve</b> function defines the shape of a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) curve.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param nknots

The number of knots in <i>knot</i>. The <i>nknots</i> parameter equals the number of control points plus the order.


### -param knot

An array of <i>nknots</i> nondecreasing knot values.


### -param stride

The offset (as a number of single-precision floating-point values) between successive curve control points.


### -param ctlarray

A pointer to an array of control points. The coordinates must agree with <i>type</i>.


### -param order

The order of the NURBS curve. The <i>order</i> parameter equals degree + 1; hence a cubic curve has an order of 4.


### -param type

The type of the curve. If this curve is defined within a <a href="https://msdn.microsoft.com/f7f2e765-1a07-4faa-940c-9cb957dd54d4">gluBeginCurve</a>/<a href="https://msdn.microsoft.com/b00ec687-6127-4585-b7b7-06e8dca78cfc">gluEndCurve</a> pair, then the type can be any of the valid one-dimensional evaluator types (such as GL_MAP1_VERTEX_3 or GL_MAP1_COLOR_4). Between a <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>/<a href="https://msdn.microsoft.com/e85cc60b-4492-441d-b778-31a3d52b398a">gluEndTrim</a> pair, the only valid types are GLU_MAP1_TRIM_2 and GLU_MAP1_TRIM_3.


## -returns



This function does not return a value.




## -remarks



When <b>gluNurbsCurve</b> appears between a <b>gluBeginCurve</b>/<b>gluEndCurve</b> pair, it describes a curve to be rendered. You associate positional, texture, and color coordinates by presenting each as a separate <b>gluNurbsCurve</b> between a <b>gluBeginCurve</b>/<b>gluEndCurve</b> pair. Do not make more than one call to <b>gluNurbsCurve</b> for color, position, and texture data within a single <b>gluBeginCurve</b>/<b>gluEndCurve</b> pair. Make exactly one call to describe the position of the curve (a <i>type</i> of GL_MAP1_VERTEX_3 or GL_MAP1_VERTEX_4).

When <b>gluNurbsCurve</b> appears between a <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>/<a href="https://msdn.microsoft.com/e85cc60b-4492-441d-b778-31a3d52b398a">gluEndTrim</a> pair, it describes a trimming curve on a NURBS surface. If <i>type</i> is GLU_MAP1_TRIM_2, it describes a curve in two-dimensional (<i>u</i> and <i>v</i>) parameter space. If it is GLU_MAP1_TRIM_3, it describes a curve in two-dimensional homogeneous (<i>u</i>, <i>v</i>, and <i>w</i>) parameter space. For more discussion about trimming curves, see <b>gluBeginTrim</b>.


#### Examples

The following functions render a textured NURBS curve with normals:

<pre class="syntax" xml:space="preserve"><code>gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); </code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f7f2e765-1a07-4faa-940c-9cb957dd54d4">gluBeginCurve</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/b00ec687-6127-4585-b7b7-06e8dca78cfc">gluEndCurve</a>



<a href="https://msdn.microsoft.com/e85cc60b-4492-441d-b778-31a3d52b398a">gluEndTrim</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>
 

 

