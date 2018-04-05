---
UID: NF:glu.gluEndTrim
title: gluEndTrim function
author: windows-driver-content
description: The gluBeginTrim and gluEndTrim functions delimit a Non-Uniform Rational B-Spline (NURBS) trimming loop definition.
old-location: opengl\gluendtrim.htm
old-project: OpenGL
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluEndTrim, gluEndTrim, gluEndTrim function [OpenGL], opengl.gluendtrim
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
-	gluEndTrim
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluEndTrim function


## -description


The <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a> and <b>gluEndTrim</b> functions delimit a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) trimming loop definition.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


## -returns



This function does not return a value.




## -remarks



Use <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a> to mark the beginning of a trimming loop, and <b>gluEndTrim</b> to mark the end of a trimming loop. A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface. You include these trimming loops in the definition of a NURBS surface, between calls to <a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a> and <a href="https://msdn.microsoft.com/beaa0340-c67d-4376-bedd-7f73c5c6d742">gluEndSurface</a>.

The definition for a NURBS surface can contain many trimming loops. For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops. One loop would define the outer edge of the rectangle; the other would define the punched-out hole. The definitions of each of these trimming loops would be bracketed by a <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a> / <b>gluEndTrim</b> pair.

The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see <a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>), as a single NURBS curve (see <a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>), or as a combination of both in any order. The only library calls that can appear in a trimming-loop definition (between the calls to <a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a> and <b>gluEndTrim</b>) are <b>gluPwlCurve</b> and <b>gluNurbsCurve</b>.

The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases. Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop. For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.

If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve). If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match. If the endpoints are not sufficiently close, an error results (see <a href="https://msdn.microsoft.com/1e9afc00-57c6-459e-a9fc-463f45df2084">gluNurbsCallback</a>).

If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves). You can use nested trimming loops as long as the curve orientations alternate correctly. Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).

If no trimming information is given for a NURBS surface, the entire surface is drawn.


#### Examples

This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:
 

<pre class="syntax" xml:space="preserve"><code>
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a>



<a href="https://msdn.microsoft.com/beaa0340-c67d-4376-bedd-7f73c5c6d742">gluEndSurface</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/1e9afc00-57c6-459e-a9fc-463f45df2084">gluNurbsCallback</a>



<a href="https://msdn.microsoft.com/d03064a5-26f5-487f-877f-3748646bcb2f">gluNurbsCurve</a>



<a href="https://msdn.microsoft.com/3d08e7e8-dfdf-447c-9795-bd73299412b5">gluPwlCurve</a>
 

 

