---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection) (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1GradientStopCollection from the specified gradient stops that uses the D2D1_GAMMA_2_2 color interpolation gamma and the clamp extend mode.
old-location: direct2d\ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_ptr_ptr_ID2D1GradientStopCollection.htm
tech.root: Direct2D
ms.assetid: 0351e843-18cc-402b-8e4d-3f834de9501a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection method [Direct2D], CreateGradientStopCollection method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateGradientStopCollection method, ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), ID2D1RenderTarget::CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection), d2d1/ID2D1RenderTarget::CreateGradientStopCollection, direct2d.ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_ptr_ptr_ID2D1GradientStopCollection
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget.CreateGradientStopCollection"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,ID2D1GradientStopCollection)


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified gradient stops that uses the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_gamma">D2D1_GAMMA_2_2</a> color interpolation gamma and the clamp extend mode.


## -parameters




### -param gradientStops [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>*</b>

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures.


### -param gradientStopsCount

Type: <b>UINT</b>

A value greater than or equal to 1 that specifies the number of gradient stops in the <i>gradientStops</i> array.


### -param gradientStopCollection [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>**</b>

When this method returns, contains a pointer to a pointer to the new gradient stop collection.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-linear-gradient-brush">How to Create a Linear Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

