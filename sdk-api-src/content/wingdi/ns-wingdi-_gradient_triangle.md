---
UID: NS:wingdi._GRADIENT_TRIANGLE
title: "_GRADIENT_TRIANGLE"
author: windows-sdk-content
description: The GRADIENT_TRIANGLE structure specifies the index of three vertices in the pVertex array in the GradientFill function. These three vertices form one triangle.
old-location: gdi\gradient_triangle.htm
tech.root: gdi
ms.assetid: 71f3a4bd-5823-47ae-aa7a-f3058f18c591
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPGRADIENT_TRIANGLE, *PGRADIENT_TRIANGLE, GRADIENT_TRIANGLE, GRADIENT_TRIANGLE structure [Windows GDI], PGRADIENT_TRIANGLE, PGRADIENT_TRIANGLE structure pointer [Windows GDI], _GRADIENT_TRIANGLE, _win32_GRADIENT_TRIANGLE_str, gdi.gradient_triangle, wingdi/GRADIENT_TRIANGLE, wingdi/PGRADIENT_TRIANGLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GRADIENT_TRIANGLE
product: Windows
targetos: Windows
req.typenames: GRADIENT_TRIANGLE, *PGRADIENT_TRIANGLE, *LPGRADIENT_TRIANGLE
req.redist: 
---

# _GRADIENT_TRIANGLE structure


## -description



The <b>GRADIENT_TRIANGLE</b> structure specifies the index of three vertices in the <i>pVertex</i> array in the <b>GradientFill</b> function. These three vertices form one triangle.




## -struct-fields




### -field Vertex1

The first point of the triangle where sides intersect.


### -field Vertex2

The second point of the triangle where sides intersect.


### -field Vertex3

The third point of the triangle where sides intersect.


## -remarks



The <b>GRADIENT_TRIANGLE</b> structure specifies the values in the <i>pVertex</i> array that are used when the <i>dwMode</i> parameter of the <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a> function is GRADIENT_FILL_TRIANGLE. For related <b>GradientFill</b> structures, see <a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a> and <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a>.

The following image shows an example of a triangle with a gradient fill.

<img alt="Illustration of a triangle that fills from orange at the top point to magenta on the bottom line " border="0" src="images/GradientFillTriangle.png"/>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/78834f92-00cb-4899-851a-1de5e3c1f4fa">Drawing a Shaded Triangle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a>



<a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>



<a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a>
 

 

