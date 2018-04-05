---
UID: NF:gl.glBlendFunc
title: glBlendFunc function
author: windows-driver-content
description: The glBlendFunc function specifies pixel arithmetic.
old-location: opengl\glblendfunc.htm
old-project: OpenGL
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glBlendFunc, gl/glBlendFunc, glBlendFunc, glBlendFunc function [OpenGL], opengl.glblendfunc"
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
-	glBlendFunc
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glBlendFunc function


## -description


The <b>glBlendFunc</b> function specifies pixel arithmetic.


## -parameters




### -param sfactor

Specifies how the red, green, blue, and alpha source-blending factors are computed. Nine symbolic constants are accepted: GL_ZERO, GL_ONE, GL_DST_COLOR, GL_ONE_MINUS_DST_COLOR, GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA, GL_DST_ALPHA, GL_ONE_MINUS_DST_ALPHA, and GL_SRC_ALPHA_SATURATE.


### -param dfactor

Specifies how the red, green, blue, and alpha destination-blending factors are computed. Eight symbolic constants are accepted: GL_ZERO, GL_ONE, GL_SRC_COLOR, GL_ONE_MINUS_SRC_COLOR, GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA, GL_DST_ALPHA, and GL_ONE_MINUS_DST_ALPHA.


## -returns



This function does not return a value.




## -remarks



In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values). By default, blending is disabled. Use <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with the GL_BLEND argument to enable and disable blending.

When enabled, <b>glBlendFunc</b> defines the operation of blending. The <i>sfactor</i> parameter specifies which of nine methods is used to scale the source color components. The <i>dfactor</i> parameter specifies which of eight methods is used to scale the destination color components. The eleven possible methods are described in the following table. Each method defines four scale factors—one each for red, green, blue, and alpha.

In the table and in subsequent equations, source and destination color components are referred to as (<i>R</i>ₛ , <i>G</i>ₛ , <i>B</i>ₛ , <i>A</i>ₛ ) and (<i>R</i><sub>d</sub> , <i>G</i><sub>d</sub> , <i>B</i><sub>d</sub> , <i>A</i><sub>d</sub> ). They are understood to have integer values between zero and (<i>k</i><sub>R</sub> , <i>k</i><sub>G</sub> , <i>k</i><sub>R</sub> , <i>k</i><sub>A</sub> ), where

<i>k</i><sub>R</sub> = 2<sup>m</sup><i>R</i> - 1

<i>k</i><sub>G</sub> = 2<sup>m</sup><i>G</i> - 1

<i>k</i><sub>B</sub> = 2<sup>m</sup><i>B</i> - 1

<i>k</i><sub>A</sub> = 2<sup>m</sup><i>A</i> - 1

and (<i>m</i><sub>R</sub> ,  <i>m</i><sub>G</sub> , <i>m</i><sub>B</sub> , <i>m</i><sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.

Source and destination scale factors are referred to as (<i>s</i><sub>R</sub> , <i>s</i><sub>G</sub> , <i>s</i><sub>B</sub> , <i>s</i><sub>A</sub> ) and (<i>d</i><sub>R</sub> , <i>d</i><sub>G</sub> , <i>d</i><sub>B</sub> , <i>d</i><sub>A</sub> ). The scale factors described in the table, denoted (<i>f</i><sub>R</sub> , <i>f</i><sub>G</sub> , <i>f</i><sub>B</sub> , <i>f</i><sub>A</sub> ), represent either source or destination factors. All scale factors have range [0,1].

<table>
<tr>
<th>Parameter</th>
<th>
              (<i>f</i><sub>R</sub> 
              , <i>f</i><sub>G</sub> 
              , <i>f</i><sub>B</sub> 
              , <i>f</i><sub>A</sub> 
              )
            </th>
</tr>
<tr>
<td>GL_ZERO</td>
<td>(0,0,0,0)</td>
</tr>
<tr>
<td>GL_ONE</td>
<td>(1,1,1,1)</td>
</tr>
<tr>
<td>GL_SRC_COLOR</td>
<td>(<i>R</i>ₛ / <i>k</i><sub>R</sub> , <i>G</i>ₛ / <i>k</i><sub>G</sub> , <i>B</i>ₛ / <i>k</i><sub>B</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_ONE_MINUS_SRC_COLOR</td>
<td>(1,1,1,1) - (<i>R</i>ₛ / <i>k</i><sub>R</sub> , <i>G</i>ₛ / <i>k</i><sub>G</sub> , <i>B</i>ₛ / <i>k</i><sub>B</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_DST_COLOR</td>
<td>(<i>R</i><sub>d</sub> / <i>k</i><sub>R</sub> , <i>G</i><sub>d</sub> / <i>k</i><sub>G</sub> , <i>B</i><sub>d</sub> / <i>k</i><sub>B</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_ONE_MINUS_DST_COLOR</td>
<td>(1,1,1,1) - (<i>R</i><sub>d</sub> / <i>k</i><sub>R</sub> , <i>G</i><sub>d</sub> / <i>k</i><sub>G</sub> , <i>B</i><sub>d</sub> / <i>k</i><sub>B</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_SRC_ALPHA</td>
<td>				
(<i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> )              
            </td>
</tr>
<tr>
<td>GL_ONE_MINUS_SRC_ALPHA</td>
<td>(1,1,1,1) - (<i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> , <i>A</i>ₛ / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_DST_ALPHA</td>
<td>(<i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_ONE_MINUS_DST_ALPHA</td>
<td>(1,1,1,1) - (<i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> , <i>A</i><sub>d</sub> / <i>k</i><sub>A</sub> )</td>
</tr>
<tr>
<td>GL_SRC_ALPHA_SATURATE</td>
<td>(<i>i,i,i,</i> 1)</td>
</tr>
</table>
 

In the table,

<i>i</i> = min (<i>A</i>ₛ , <i>k</i><sub>A</sub>  -<i> A</i><sub>d</sub> ) / <i>k</i><sub>A</sub>

To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:

<i>R</i> (<i>d</i>) = min( <i>k</i><sub>R</sub> , <i>R</i>ₛ <i>s</i><sub>R</sub> + <i>R</i><sub>d</sub> <i>d</i><sub>R</sub> )

<i>G</i> (<i>d</i>) = min( <i>k</i><sub>G</sub> , <i>G</i>ₛ <i>s</i><sub>G</sub> + <i>G</i><sub>d</sub> <i>d</i><sub>G</sub>  )

<i>B</i> (<i>d</i>) = min( <i>k</i><sub>B</sub> <i>, B</i>ₛ <i>s</i><sub>B</sub> + <i>B</i><sub>d</sub> <i>d</i><sub>B</sub>  )

<i>A</i> (<i>d</i>) = min( <i>k</i><sub>A</sub> , <i>A</i>ₛ <i>s</i><sub>A</sub> + <i>A</i><sub>d</sub> <i>d</i><sub>A</sub>  )

Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values. However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero. Thus, for example, when <i>sfactor</i> is GL_SRC_ALPHA, <i>dfactor</i> is GL_ONE_MINUS_SRC_ALPHA, and <i>A</i>ₛ is equal to <i>k</i><sub>A</sub>, the equations reduce to simple replacement:

<i>R</i><sub>d</sub> = <i>R</i>ₛ

<i>G</i><sub>d</sub> = <i>G</i>ₛ

<i></i>B<sub>d</sub> = <i>B</i>ₛ

<i>A</i><sub>d</sub> = <i>A</i>ₛ


#### Examples

Transparency is best implemented using <b>glBlendFunc</b>(GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA) with primitives sorted from farthest to nearest. Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.

You can also use <b>glBlendFunc</b>(GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA) for rendering antialiased points and lines in arbitrary order.

To optimize polygon antialiasing, use <b>glBlendFunc</b>(GL_SRC_ALPHA_SATURATE, GL_ONE) with polygons sorted from nearest to farthest. (See the GL_POLYGON_SMOOTH argument in <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.

Incoming (source) alpha is a material opacity, ranging from 1.0 (<i>K</i><sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.

When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color. (See <a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>.)

Blending affects only RGBA rendering. It is ignored by color-index renderers.

The following functions retrieve information related to <b>glBlendFunc</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_BLEND_SRC



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_BLEND_DST



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>  with argument GL_BLEND

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>
 

 

