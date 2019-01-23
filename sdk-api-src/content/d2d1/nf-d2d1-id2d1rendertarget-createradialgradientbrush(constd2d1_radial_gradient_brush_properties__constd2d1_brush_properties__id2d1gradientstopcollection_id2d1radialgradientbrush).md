---
UID: NF:d2d1.ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)
title: ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)
author: windows-sdk-content
description: Creates an ID2D1RadialGradientBrush that contains the specified gradient stops and has the specified transform and base opacity.
old-location: direct2d\ID2D1RenderTarget_CreateRadialGradientBrush_overload1.htm
tech.root: Direct2D
ms.assetid: df87e288-392d-439e-8d03-e4866fde892f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush method [Direct2D], CreateRadialGradientBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateRadialGradientBrush method, ID2D1RenderTarget.CreateRadialGradientBrush, ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), ID2D1RenderTarget::CreateRadialGradientBrush, ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), d2d1/ID2D1RenderTarget::CreateRadialGradientBrush, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_overload1, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_ref_D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1RadialGradientBrush
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
 - ID2D1RenderTarget.CreateRadialGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)


## -description


Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.


## -parameters




### -param radialGradientBrushProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/194f7624-ac3b-4054-8d6f-5b4c99ef6546">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a></b>

The center, gradient origin offset, and x-radius and y-radius of the brush's gradient.


### -param brushProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a></b>

The transform and base opacity of the new brush.


### -param gradientStopCollection [in]

Type: <b><a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>*</b>

A collection of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures that describe the colors in the brush's gradient and their locations along the gradient.


### -param radialGradientBrush [out]

Type: <b><a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

