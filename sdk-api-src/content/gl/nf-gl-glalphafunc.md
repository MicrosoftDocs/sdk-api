---
UID: NF:gl.glAlphaFunc
title: glAlphaFunc function
author: windows-driver-content
description: The glAlphaFunc function enables your application to set the alpha test function.
old-location: opengl\glalphafunc.htm
old-project: OpenGL
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALWAYS, GL_EQUAL, GL_GEQUAL, GL_GREATER, GL_LEQUAL, GL_LESS, GL_NEVER, GL_NOTEQUAL, _ogl_glAlphaFunc, gl/glAlphaFunc, glAlphaFunc, glAlphaFunc function [OpenGL], opengl.glalphafunc
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
-	glAlphaFunc
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glAlphaFunc function


## -description


The <b>glAlphaFunc</b> function enables your application to set the alpha test function.


## -parameters




### -param func

The alpha comparison function. The following are the accepted symbolic constants and their meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_NEVER"></a><a id="gl_never"></a><dl>
<dt><b>GL_NEVER</b></dt>
</dl>
</td>
<td width="60%">
Never passes.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LESS"></a><a id="gl_less"></a><dl>
<dt><b>GL_LESS</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is less than the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EQUAL"></a><a id="gl_equal"></a><dl>
<dt><b>GL_EQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is equal to the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LEQUAL"></a><a id="gl_lequal"></a><dl>
<dt><b>GL_LEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is less than or equal to the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREATER"></a><a id="gl_greater"></a><dl>
<dt><b>GL_GREATER</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is greater than the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NOTEQUAL"></a><a id="gl_notequal"></a><dl>
<dt><b>GL_NOTEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is not equal to the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GEQUAL"></a><a id="gl_gequal"></a><dl>
<dt><b>GL_GEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming alpha value is greater than or equal to the reference value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALWAYS"></a><a id="gl_always"></a><dl>
<dt><b>GL_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Always passes. This is the default.

</td>
</tr>
</table>
 


### -param ref

The reference value to which incoming alpha values are compared. This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value. The default reference is 0.


## -returns



This function does not return a value.




## -remarks



The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value. 
      The <b>glAlphaFunc</b> function specifies the reference and comparison function. The comparison is performed only if alpha testing is enabled.
      (For more information on GL_ALPHA_TEST, see <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>.)

The <i>func</i> and <i>ref</i> parameters specify the conditions under which the pixel is drawn. The incoming alpha value is compared 
      to <i>ref</i> using the function specified by <i>func</i>. If the comparison passes, the incoming fragment is drawn, conditional on subsequent 
      stencil and depth-buffer tests. If the comparison fails, no change is made to the framebuffer at that pixel location.

The <b>glAlphaFunc</b> function operates on all pixel writes, including those resulting from the scan conversion of points, lines,
      polygons, and bitmaps, and from pixel draw and copy operations. The <b>glAlphaFunc</b> function does not affect screen clear operations.

Alpha testing is done only in RGBA mode.

The following functions retrieve information related to the <b>glAlphaFunc</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ALPHA_TEST_FUNC

<b>glGet</b> with argument GL_ALPHA_TEST_REF


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_ALPHA_TEST




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>
 

 

