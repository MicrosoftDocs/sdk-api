---
UID: NF:d2d1.ID2D1RenderTarget.CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush)
title: ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush)
author: windows-sdk-content
description: Creates an ID2D1LinearGradientBrush that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
old-location: direct2d\ID2D1RenderTarget_CreateLinearGradientBrush_overload2.htm
tech.root: Direct2D
ms.assetid: b13314ca-3b0b-4d51-99cc-0a56eae223f1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateLinearGradientBrush, CreateLinearGradientBrush method [Direct2D], CreateLinearGradientBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLinearGradientBrush method, ID2D1RenderTarget.CreateLinearGradientBrush, ID2D1RenderTarget.CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush), ID2D1RenderTarget::CreateLinearGradientBrush, ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush), d2d1/ID2D1RenderTarget::CreateLinearGradientBrush, direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_overload2, direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_ref_D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1LinearGradientBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.CreateLinearGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush)


## -description


Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
    


## -parameters




### -param linearGradientBrushProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/753278f0-d8a1-4dc5-b976-a00f8aab357e">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a></b>

The start and end points of the gradient.


### -param gradientStopCollection [in]

Type: <b><a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>*</b>

A collection of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures that describe the colors in the brush's gradient and their locations along the gradient line.


### -param linearGradientBrush [out]

Type: <b><a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>**</b>

When this method returns, contains the address of a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>



<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>



<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

