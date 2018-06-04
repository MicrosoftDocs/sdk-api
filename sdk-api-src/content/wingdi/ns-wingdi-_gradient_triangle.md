---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

