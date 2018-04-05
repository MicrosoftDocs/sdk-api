---
UID: NF:glu.gluNurbsSurface
title: gluNurbsSurface function
author: windows-driver-content
description: The gluNurbsSurface function defines the shape of a Non-Uniform Rational B-Spline (NURBS) surface.
old-location: opengl\glunurbssurface.htm
old-project: OpenGL
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluNurbsSurface, glu/gluNurbsSurface, gluNurbsSurface, gluNurbsSurface function [OpenGL], opengl.glunurbssurface"
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
-	gluNurbsSurface
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNurbsSurface function


## -description


The <b>gluNurbsSurface</b> function defines the shape of a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) surface.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param sknot_count

The number of knots in the parametric <i>u</i> direction.


### -param sknot

An array of <i>sknot_count</i> nondecreasing knot values in the parametric <i>u</i> direction.


### -param tknot_count

The number of knots in the parametric <i>v</i> direction.


### -param tknot

An array of <i>tknot_count</i> nondecreasing knot values in the parametric <i>v</i> direction.


### -param s_stride

The offset (as a number of single precisionfloating-point values) between successive control points in the parametric <i>u</i> direction in <i>ctlarray</i>.


### -param t_stride

The offset (in single precisionfloating-point values) between successive control points in the parametric <i>v</i> direction in <i>ctlarray</i>.


### -param ctlarray

An array containing control points for the NURBS surface. The offsets between successive control points in the parametric <i>u</i> and <i>v</i> directions are given by <i>s_stride</i> and <i>t_stride</i>.


### -param sorder

The order of the NURBS surface in the parametric <i>u</i> direction. The order is one more than the degree, hence a surface that is cubic in <i>u</i> has a <i>u</i> order of 4.


### -param torder

The order of the NURBS surface in the parametric <i>v</i> direction. The order is one more than the degree, hence a surface that is cubic in <i>v</i> has a <i>v</i> order of 4.


### -param type

The type of the surface. The <i>type</i> parameter can be any of the valid two-dimensional evaluator types (such as GL_MAP2_VERTEX_3 or GL_MAP2_COLOR_4).


## -returns



This function does not return a value.




## -remarks



Use <b>gluNurbsSurface</b> within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming). To mark the beginning of a NURBS surface definition, use the <a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a> function. To mark the end of a NURBS surface definition, use the <a href="https://msdn.microsoft.com/beaa0340-c67d-4376-bedd-7f73c5c6d742">gluEndSurface</a> function. Call <b>gluNurbsSurface</b> within a NURBS surface definition only.

You associate positional, texture, and color coordinates with a surface by presenting each as a separate <b>gluNurbsSurface</b> between a <b>gluBeginSurface</b>/<b>gluEndSurface</b> pair. Within a single <b>gluBeginSurface</b>/<b>gluEndSurface</b> pair, you can make only one call to <b>gluNurbsSurface</b> for color, position, and texture data. Make exactly one call to describe the position of the surface (a <i>type</i> of GL_MAP2_VERTEX_3 or GL_MAP2_VERTEX_4).

You can trim a NURBS surface by using the <a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a> and <a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a> functions between calls to <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a> and <a href="https://msdn.microsoft.com/e85cc60b-4492-441d-b778-31a3d52b398a">gluEndTrim</a>.


        A <b>gluNurbsSurface</b> with <i>sknot_count</i> knots in the <i>u</i> direction and <i>tknot_count</i> knots in the <i>v</i> direction with orders <i>sorder</i> and <i>torder</i> must have (<i>sknot_count</i> -<i>sorder</i>) multipied by (<i>tknot_count</i> -<i>torder</i>) control points.




## -see-also




<a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/beaa0340-c67d-4376-bedd-7f73c5c6d742">gluEndSurface</a>



<a href="https://msdn.microsoft.com/e85cc60b-4492-441d-b778-31a3d52b398a">gluEndTrim</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>



<a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>
 

 

