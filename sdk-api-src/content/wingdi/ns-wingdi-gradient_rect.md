---
UID: NS:wingdi._GRADIENT_RECT
title: GRADIENT_RECT (wingdi.h)
author: windows-sdk-content
description: The GRADIENT_RECT structure specifies the index of two vertices in the pVertex array in the GradientFill function. These two vertices form the upper-left and lower-right boundaries of a rectangle.
old-location: gdi\gradient_rect.htm
tech.root: gdi
ms.assetid: 8660114a-423f-40a8-b113-e0304bb0f383
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPGRADIENT_RECT, *PGRADIENT_RECT, GRADIENT_RECT, GRADIENT_RECT structure [Windows GDI], PGRADIENT_RECT, PGRADIENT_RECT structure pointer [Windows GDI], _win32_GRADIENT_RECT_str, gdi.gradient_rect, wingdi/GRADIENT_RECT, wingdi/PGRADIENT_RECT"
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
 - GRADIENT_RECT
product: Windows
targetos: Windows
req.typenames: GRADIENT_RECT, *PGRADIENT_RECT, *LPGRADIENT_RECT
req.redist: 
ms.custom: 19H1
---

# GRADIENT_RECT structure


## -description



The <b>GRADIENT_RECT</b> structure specifies the index of two vertices in the <i>pVertex</i> array in the <b>GradientFill</b> function. These two vertices form the upper-left and lower-right boundaries of a rectangle.




## -struct-fields




### -field UpperLeft

The upper-left corner of a rectangle.


### -field LowerRight

The lower-right corner of a rectangle.


## -remarks



The <b>GRADIENT_RECT</b> structure specifies the values of the <i>pVertex</i> array that are used when the <i>dwMode</i> parameter of the <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a> function is GRADIENT_FILL_RECT_H or GRADIENT_FILL_RECT_V. For related <b>GradientFill</b> structures, see <a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a> and <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a>.

The following images shows examples of a rectangle with a gradient fill - one in horizontal mode, the other in vertical mode.

<img alt="Illustration of a rectangle that shades from dark on the left side to light on the right side" border="0" src="images/GradientFillRectangle.png"/>
<img alt="Illustration of a rectangle that shades from dark on the top to light on the bottom" border="0" src="images/GradientFillRectangle2.png"/>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/a4277e22-03f8-470f-87e9-5aeab258b6d2">Drawing a Shaded Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a>



<a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>



<a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a>
 

 

