---
UID: NS:d2d1.D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES
title: D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES
author: windows-sdk-content
description: Contains the starting point and endpoint of the gradient axis for an ID2D1LinearGradientBrush.
old-location: direct2d\D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES.htm
tech.root: direct2d
ms.assetid: 753278f0-d8a1-4dc5-b976-a00f8aab357e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES, D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES, direct2d.D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - d2d1.h
api_name:
 - D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES
req.redist: 
---

# D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES structure


## -description


Contains the starting point and endpoint of the gradient axis for an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>. 


## -struct-fields




### -field startPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the starting point  of the gradient axis. 


### -field endPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the endpoint  of the gradient axis.  


## -remarks



Use this method when creating new <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> objects with the <a href="https://msdn.microsoft.com/dc07113f-ff93-4b0f-8328-02dd481dccb0">CreateLinearGradientBrush</a> method. For convenience, Direct2D provides the <a href="https://msdn.microsoft.com/dba59936-2b2d-4a9b-aba4-acb6ff84c037">D2D1::LinearGradientBrushProperties</a> helper function for creating new <b>D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</b> structures.

The following illustration shows how a linear gradient changes as you change its start and end points.  For the first gradient, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted. When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created. Similarly, setting the start point  to (75, 0) and the end point to (75, 50) creates a vertical gradient. Setting the start point to  (0, 50) and the end point to (150, 0)  creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.

<img alt="Illustration of four gradients with different axes" src="./images/Linear_Gradients.png"/>


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/dc07113f-ff93-4b0f-8328-02dd481dccb0">CreateLinearGradientBrush</a> method to create an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> (<i>m_pLinearGradientBrush</i>). It uses the <a href="https://msdn.microsoft.com/dba59936-2b2d-4a9b-aba4-acb6ff84c037">D2D1::LinearGradientBrushProperties</a> helper method to create a <b>D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</b> structure that contains a start point of (0, 0) and and end point of (150, 150) and passes it to the  <b>CreateLinearGradientBrush</b> method.


```cpp
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}

```


For more information about creating and using linear gradient brushes, see 
        the <a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a> topic and 
        the <a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>
 

 

