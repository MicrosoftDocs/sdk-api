---
UID: NF:glu.gluEndSurface
title: gluEndSurface function
author: windows-driver-content
description: The gluBeginSurface and gluEndSurface functions delimit a Non-Uniform Rational B-Spline (NURBS) surface definition.
old-location: opengl\gluendsurface.htm
old-project: OpenGL
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluEndSurface, gluEndSurface, gluEndSurface function [OpenGL], opengl.gluendsurface
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
-	gluEndSurface
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluEndSurface function


## -description


The <a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a> and <b>gluEndSurface</b> functions delimit a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) surface definition.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a> and <b>gluEndSurface</b> functions mark the beginning and end of NURBS surface definitions, which are defined with calls to <b>gluNurbsSurface</b>.

<ol>
<li>Call <b>gluBeginSurface</b> to mark the beginning of a NURBS surface definition.</li>
<li>Make one or more calls to <b>gluNurbsSurface</b> to define the attributes of the surface.Exactly one of these calls to <b>gluNurbsSurface</b> must have a surface type of GL_MAP2_VERTEX_3 or GL_MAP2_VERTEX_4.

</li>
<li>To mark the end of the NURBS surface definition, call <b>gluEndSurface</b>.</li>
</ol>
The <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>, <a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>, <a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>, and <b>gluEndTrim</b> functions support trimming of NURBS surfaces.

Use OpenGL evaluators to render the NURBS surface as a set of polygons. Preserve the evaluator state during rendering with <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> (GL_EVAL_BIT) and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>.


#### Examples

The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:

<pre class="syntax" xml:space="preserve"><code>gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f7f2e765-1a07-4faa-940c-9cb957dd54d4">gluBeginCurve</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>



<a href="https://msdn.microsoft.com/ee86376c-26ba-49a9-b0b0-4ca936b6614b">gluNurbsSurface</a>



<a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>
 

 

