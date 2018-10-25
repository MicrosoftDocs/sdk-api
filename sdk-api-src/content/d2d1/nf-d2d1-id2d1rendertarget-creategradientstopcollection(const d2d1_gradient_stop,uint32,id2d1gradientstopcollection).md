---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)
author: windows-sdk-content
description: Creates an ID2D1GradientStopCollection from the specified gradient stops that uses the D2D1_GAMMA_2_2 color interpolation gamma and the clamp extend mode.
old-location: direct2d\ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_ptr_ptr_ID2D1GradientStopCollection.htm
tech.root: direct2d
ms.assetid: 0351e843-18cc-402b-8e4d-3f834de9501a
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection method [Direct2D], CreateGradientStopCollection method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateGradientStopCollection method, ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), ID2D1RenderTarget::CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), d2d1/ID2D1RenderTarget::CreateGradientStopCollection, direct2d.ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_ptr_ptr_ID2D1GradientStopCollection
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
 - ID2D1RenderTarget.CreateGradientStopCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)


## -description


Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified gradient stops that uses the <a href="https://msdn.microsoft.com/c84c66c6-5f4a-41de-938c-76a409145971">D2D1_GAMMA_2_2</a> color interpolation gamma and the clamp extend mode.


## -parameters




### -param gradientStops [in]

Type: <b><a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures.


### -param gradientStopsCount

Type: <b>UINT</b>

A value greater than or equal to 1 that specifies the number of gradient stops in the <i>gradientStops</i> array.


### -param gradientStopCollection [out]

Type: <b><a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>**</b>

When this method returns, contains a pointer to a pointer to the new gradient stop collection.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>



<a href="https://msdn.microsoft.com/3cf5acc6-2f17-49d4-aca5-a84a846d1749">How to Create a Linear Gradient Brush</a>



<a href="https://msdn.microsoft.com/663743c9-16e9-4e3a-90b2-883ef0b8d5cf">How to Create a Radial Gradient Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

