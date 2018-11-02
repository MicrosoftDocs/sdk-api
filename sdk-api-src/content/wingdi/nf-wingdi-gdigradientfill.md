---
UID: NF:wingdi.GdiGradientFill
title: GdiGradientFill function
author: windows-sdk-content
description: The GdiGradientFill function fills rectangle and triangle structures.
old-location: gdi\gdigradientfill.htm
tech.root: gdi
ms.assetid: c88c1137-5690-4139-9d10-90d036e8f31c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GRADIENT_FILL_RECT_H, GRADIENT_FILL_RECT_V, GRADIENT_FILL_TRIANGLE, GdiGradientFill, GdiGradientFill function [Windows GDI], gdi.gdigradientfill, wingdi/GdiGradientFill
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GdiGradientFill
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GdiGradientFill function


## -description


The <b>GdiGradientFill</b> function fills rectangle and triangle structures.


## -parameters




### -param hdc [in]

A handle to the destination device context.


### -param pVertex [in]

A pointer to an array of <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structures that each define a triangle vertex.


### -param nVertex [in]

The number of vertices in <i>pVertex</i>.


### -param pMesh [in]

An array of <a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a> structures in triangle mode, or an array of <a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a> structures in rectangle mode.


### -param nCount [in]

The number of elements (triangles or rectangles) in <i>pMesh</i>.


### -param ulMode [in]

The gradient fill mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_H"></a><a id="gradient_fill_rect_h"></a><dl>
<dt><b>GRADIENT_FILL_RECT_H</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structure) for the left and right edges. GDI interpolates the color from the left to right edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_V"></a><a id="gradient_fill_rect_v"></a><dl>
<dt><b>GRADIENT_FILL_RECT_V</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structure) for the top and bottom edges. GDI interpolates the color from the top to bottom edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_TRIANGLE"></a><a id="gradient_fill_triangle"></a><dl>
<dt><b>GRADIENT_FILL_TRIANGLE</b></dt>
</dl>
</td>
<td width="60%">
In this mode, an array of <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structures is passed to GDI along with a list of array indexes that describe separate triangles. GDI performs linear interpolation between triangle vertices and fills the interior. Drawing is done directly in 24- and 32-bpp modes. Dithering is performed in 16-, 8-, 4-, and 1-bpp mode.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  This function is the same as <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>.</div>
<div> </div>
To add smooth shading to a triangle, call the <b>GdiGradientFill</b> function with the three triangle endpoints. GDI will linearly interpolate and fill the triangle. Here is the drawing output of a shaded triangle.

<img alt="Illustration of a triangle that fills from orange at the top point to magenta on the bottom line " border="0" src="./images/GradientFillTriangle.png"/>
To add smooth shading to a rectangle, call <b>GdiGradientFill</b> with the upper-left and lower-right coordinates of the rectangle. There are two shading modes used when drawing a rectangle. In horizontal mode, the rectangle is shaded from left-to-right. In vertical mode, the rectangle is shaded from top-to-bottom. Here is the drawing output of two shaded rectangles - one in horizontal mode, the other in vertical mode.

<img alt="Illustration of a rectangle that shades from dark on the left side to light on the right side" border="0" src="./images/GradientFillRectangle.png"/>
<img alt="Illustration of a rectangle that shades from dark on the top to light on the bottom" border="0" src="./images/GradientFillRectangle2.png"/>
The <b>GdiGradientFill</b> function uses a mesh method to specify the endpoints of the object to draw. All vertices are passed to <b>GdiGradientFill</b> in the <i>pVertex</i> array. The <i>pMesh</i> parameter specifies how these vertices are connected to form an object. When filling a rectangle, <i>pMesh</i> points to an array of <a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a> structures. Each <b>GRADIENT_RECT</b> structure specifies the index of two vertices in the <i>pVertex</i> array. These two vertices form the upper-left and lower-right boundary of one rectangle.

In the case of filling a triangle, <i>pMesh</i> points to an array of <a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a> structures. Each <b>GRADIENT_TRIANGLE</b> structure specifies the index of three vertices in the <i>pVertex</i> array. These three vertices form one triangle.

To simplify hardware acceleration, this routine is not required to be pixel-perfect in the triangle interior.

Note that <b>GdiGradientFill</b> does not use the Alpha member of the <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structure. To use <b>GdiGradientFill</b> with transparency, call <b>GdiGradientFill</b> and then call <a href="https://msdn.microsoft.com/703d2a6a-0f3f-4f8f-90bd-e1e821dfbcde">GdiAlphaBlend</a> with the desired values for the alpha channel of each vertex.

For more information, see <a href="https://msdn.microsoft.com/94f26d15-fb76-47ec-b805-f04975d41b43">Smooth Shading</a>, <a href="https://msdn.microsoft.com/78834f92-00cb-4899-851a-1de5e3c1f4fa">Drawing a Shaded Triangle</a>, and <a href="https://msdn.microsoft.com/a4277e22-03f8-470f-87e9-5aeab258b6d2">Drawing a Shaded Rectangle</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/efd12e71-ee26-4fc8-8e9f-5b0105ebe057">EMRGRADIENTFILL</a>



<a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a>



<a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a>



<a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a>
 

 

