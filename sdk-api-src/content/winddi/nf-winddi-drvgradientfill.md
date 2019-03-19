---
UID: NF:winddi.DrvGradientFill
title: DrvGradientFill function (winddi.h)
author: windows-sdk-content
description: The DrvGradientFill function shades the specified primitives.
old-location: display\drvgradientfill.htm
tech.root: display
ms.assetid: c8a51b5f-5509-4801-8432-c4d895cefbda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrvGradientFill, DrvGradientFill function [Display Devices], ddifncs_23385260-cc1d-4871-8aad-b6618e3d5f52.xml, display.drvgradientfill, winddi/DrvGradientFill
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvGradientFill
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvGradientFill function


## -description


The <b>DrvGradientFill</b> function shades the specified primitives.


## -parameters




### -param psoDest [in, out]

Pointer to the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that identifies the surface on which to draw.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved.


### -param pxlo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure. This parameter should be ignored by the driver.


### -param pVertex [in]

Pointer to an array of TRIVERTEX structures, with each entry containing position and color information. The TRIVERTEX structure is described in the Microsoft Windows SDK documentation.


### -param nVertex [in]

Specifies the number of TRIVERTEX structures in the array to which <i>pVertex</i> points.


### -param pMesh [in]

Pointer to an array of structures that define the connectivity of the TRIVERTEX elements to which <i>pVertex</i> points.

When rectangles are being drawn, <i>pMesh</i> points to an array of GRADIENT_RECT structures, each of which specifies two TRIVERTEX elements that define a rectangle. The TRIVERTEX elements can represent any diagonally-opposed pair of rectangle vertices. Rectangle drawing is lower-right exclusive. Both TRIVERTEX and GRADIENT_RECT are defined in the Windows SDK documentation.

When triangles are being drawn, <i>pMesh</i> points to an array of GRADIENT_TRIANGLE structures, each of which specifies the three TRIVERTEX elements that define a triangle. Triangle drawing is lower-right exclusive. GRADIENT_TRIANGLE is defined in the Windows SDK documentation.


### -param nMesh [in]

Specifies the number of elements in the array to which <i>pMesh</i> points.


### -param prclExtents [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the area in which the gradient drawing is to occur. The points are specified in the coordinate system of the destination surface. This parameter is useful in estimating the size of the drawing operations.


### -param pptlDitherOrg [in]

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the origin on the surface for dithering. The upper left pixel of the dither pattern is aligned with this point.


### -param ulMode [in]

Specifies the current drawing mode and how to interpret the array to which <i>pMesh</i> points. This parameter can be one of the following values:





#### GRADIENT_FILL_RECT_H

The <i>pMesh</i> parameter points to an array of GRADIENT_RECT structures. Each rectangle is to be shaded from left to right. Specifically, the upper-left and lower-left pixels are the same color, as are the upper-right and lower-right pixels.



#### GRADIENT_FILL_RECT_V

The <i>pMesh</i> parameter points to an array of GRADIENT_RECT structures. Each rectangle is to be shaded from top to bottom. Specifically, the upper-left and upper-right pixels are the same color, as are the lower-left and lower-right pixels.



#### GRADIENT_FILL_TRIANGLE

The <i>pMesh</i> parameter points to an array of GRADIENT_TRIANGLE structures.

The <a href="https://msdn.microsoft.com/f67c673d-c6f0-49f0-850a-d8b00e99ddd4">gradient fill</a> calculations for each mode are documented in the Remarks section.


## -returns



<b>DrvGradientFill</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b> and reports an error by calling <a href="https://msdn.microsoft.com/8887eed8-c60d-4217-92bf-f770be071c49">EngSetLastError</a>.




## -remarks



<b>DrvGradientFill</b> can be optionally implemented in graphics drivers. GDI never calls this function for palletized surfaces.

The driver hooks <b>DrvGradientFill</b> by setting the HOOK_GRADIENTFILL flag when it calls <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a> or <a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>. If the driver has hooked <b>DrvGradientFill</b> and is called to perform an operation that it does not support, the driver should have GDI handle the operation by punting the data in a call to <a href="https://msdn.microsoft.com/1005f89f-65cf-49bb-8377-3581fdc9c654">EngGradientFill</a>.

GDI will not call <b>DrvGradientFill</b> for 8bpp destination surfaces.

The formulas for computing the color value at each pixel of the primitive depend on <i>ulMode</i> as follows:



The total error accumulated over all three color channels must not be more than eight (8). For more information about permissible error, see <a href="https://msdn.microsoft.com/f44a89df-6412-442c-8491-3e2f2bbd826f">Special Effects in Display Drivers</a>.

The driver should ignore the alpha value of the vertices, leaving the alpha channel unchanged for surfaces that support alpha blending.




## -see-also




<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>



<a href="https://msdn.microsoft.com/1005f89f-65cf-49bb-8377-3581fdc9c654">EngGradientFill</a>
 

 

