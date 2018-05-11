---
UID: NF:winddi.EngGradientFill
title: EngGradientFill function
author: windows-driver-content
description: The EngGradientFill function shades the specified primitives.
old-location: display\enggradientfill.htm
old-project: display
ms.assetid: 1005f89f-65cf-49bb-8377-3581fdc9c654
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EngGradientFill, EngGradientFill function [Display Devices], display.enggradientfill, gdifncs_7f0502d6-5e1b-4780-9e59-3bbddf29d7c7.xml, winddi/EngGradientFill
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngGradientFill
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngGradientFill function


## -description


The <b>EngGradientFill</b> function shades the specified primitives.


## -parameters




### -param psoDest

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that identifies the surface on which to draw.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved.


### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure. This structure indicates how color indices should be translated between 32 bpp RGB format and the destination. The driver is responsible for converting the input COLOR16 color values to RGB.


### -param pVertex

Pointer to an array of TRIVERTEX structures, with each entry containing position and color information. The TRIVERTEX structure is described in the Microsoft Windows SDK documentation.


### -param nVertex

Specifies the number of TRIVERTEX structures in the array to which <i>pVertex</i> points.


### -param pMesh

Pointer to an array of structures that define the connectivity of the TRIVERTEX elements to which <i>pVertex</i> points.

When rectangles are being drawn, <i>pMesh</i> points to an array of GRADIENT_RECT structures, each of which specifies two TRIVERTEX elements that define a rectangle. The TRIVERTEX elements can represent any diagonally-opposed pair of rectangle vertices. Rectangle drawing is lower-right exclusive. Both TRIVERTEX and GRADIENT_RECT are defined in the Windows SDK documentation.

When triangles are being drawn, <i>pMesh</i> points to an array of GRADIENT_TRIANGLE structures, each of which specifies the three TRIVERTEX elements that define a triangle. Triangle drawing is lower-right exclusive. The GRADIENT_TRIANGLE structure is defined in the Windows SDK documentation.


### -param nMesh

Specifies the number of elements in the array to which <i>pMesh</i> points.


### -param prclExtents

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines the area in which the gradient drawing is to occur. The points are specified in the coordinate system of the destination surface. This parameter is useful in estimating the size of the drawing operations.


### -param pptlDitherOrg

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the origin on the surface for dithering. The upper-left pixel of the dither pattern is aligned with this point.


### -param ulMode [in]

Specifies the current drawing mode and how to interpret the array to which <i>pMesh</i> points. This parameter can be one of the following values:





#### GRADIENT_FILL_RECT_H

The <i>pMesh</i> parameter points to an array of GRADIENT_RECT structures. Each rectangle is to be shaded from left to right.



#### GRADIENT_FILL_RECT_V

The <i>pMesh</i> parameter points to an array of GRADIENT_RECT structures. Each rectangle is to be shaded from top to bottom.



#### GRADIENT_FILL_TRIANGLE

The <i>pMesh</i> parameter points to an array of GRADIENT_TRIANGLE structures.


## -returns



<b>EngGradientFill</b> returns <b>TRUE</b> upon success. Otherwise, it reports an error and returns <b>FALSE</b>.




## -remarks



The driver should call <b>EngGradientFill</b> if it has hooked <a href="https://msdn.microsoft.com/library/windows/hardware/ff556236">DrvGradientFill</a> and it is called to do something that it does not support.

The formulas used to compute the color value at each pixel depend on the value of <i>ulMode</i> as follows:



GDI ignores the alpha value of the vertices, leaving the alpha channel unchanged for surfaces that support alpha.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556236">DrvGradientFill</a>
 

 

