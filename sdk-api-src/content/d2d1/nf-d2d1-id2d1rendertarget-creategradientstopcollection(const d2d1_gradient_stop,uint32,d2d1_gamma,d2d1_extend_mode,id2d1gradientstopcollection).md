---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection)
author: windows-sdk-content
description: Creates an ID2D1GradientStopCollection from the specified gradient stops, color interpolation gamma, and extend mode.
old-location: direct2d\ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_D2D1_GAMMA_D2D1_EXTEND_MODE_ptr_ptr_ID2D1GradientStopCollection.htm
tech.root: direct2d
ms.assetid: c5f3facf-f1fe-4a47-b283-c0c859d8bc03
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection method [Direct2D], CreateGradientStopCollection method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateGradientStopCollection method, ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection), ID2D1RenderTarget::CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection), d2d1/ID2D1RenderTarget::CreateGradientStopCollection, direct2d.ID2D1RenderTarget_CreateGradientStopCollection_ptr_D2D1_GRADIENT_STOP_D2D1_GAMMA_D2D1_EXTEND_MODE_ptr_ptr_ID2D1GradientStopCollection
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

# ID2D1RenderTarget::CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection)


## -description


Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified gradient stops, color interpolation gamma, and extend mode.  


## -parameters




### -param gradientStops [in]

Type: <b>const <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>*</b>

A pointer to an array of D2D1_GRADIENT_STOP structures.


### -param gradientStopsCount

Type: <b>UINT</b>

A value greater than or equal to 1 that specifies the number of gradient stops in the <i>gradientStops</i> array.


### -param colorInterpolationGamma

Type: <b><a href="https://msdn.microsoft.com/c84c66c6-5f4a-41de-938c-76a409145971">D2D1_GAMMA</a></b>

The space in which color interpolation between the gradient stops is performed.


### -param extendMode

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The behavior of the gradient outside the [0,1] normalized range.


### -param gradientStopCollection [out]

Type: <b><a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>**</b>

When this method returns, contains a pointer to a pointer to the new gradient stop collection.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

