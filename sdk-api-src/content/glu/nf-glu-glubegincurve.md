---
UID: NF:glu.gluBeginCurve
title: gluBeginCurve function
author: windows-driver-content
description: The gluBeginCurve and gluEndCurve functions delimit a Non-Uniform Rational B-Spline (NURBS) curve definition.
old-location: opengl\glubegincurve.htm
old-project: OpenGL
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluBeginCurve, gluBeginCurve, gluBeginCurve function [OpenGL], opengl.glubegincurve
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
-	gluBeginCurve
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluBeginCurve function


## -description


The <b>gluBeginCurve</b> and <a href="https://msdn.microsoft.com/b00ec687-6127-4585-b7b7-06e8dca78cfc">gluEndCurve</a> functions delimit a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) curve definition.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


## -returns



This function does not return a value.




## -remarks



Use <b>gluBeginCurve</b> to mark the beginning of a NURBS curve definition. After calling <b>gluBeginCurve</b>, make one or more calls to <a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a> to define the attributes of the curve. Exactly one of the calls to <b>gluNurbsCurve</b> must have a curve type of GL_MAP1_VERTEX_3 or GL_MAP1_VERTEX_4. To mark the end of the NURBS curve definition, call <a href="https://msdn.microsoft.com/b00ec687-6127-4585-b7b7-06e8dca78cfc">gluEndCurve</a>.

OpenGL evaluators are used to render the NURBS curve as a series of line segments. Evaluator state is preserved during rendering with <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> (GL_EVAL_BIT) and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>. For information on exactly what state these calls preserve, see <b>glPushAttrib</b>.


#### Examples

The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:

<pre class="syntax" xml:space="preserve"><code>gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>
 

 

