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

# CreateLinearGradientBrush function


## -description


<span>Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> object for painting areas with a linear gradient.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b13314ca-3b0b-4d51-99cc-0a56eae223f1">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b8f643-de7d-4050-a1a2-4b7e73645fcc">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES&,D2D1_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/052e8292-3ce8-4ae6-a220-0271f14b5375">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES*,D2D1_BRUSH_PROPERTIES*,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>



<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>



<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

