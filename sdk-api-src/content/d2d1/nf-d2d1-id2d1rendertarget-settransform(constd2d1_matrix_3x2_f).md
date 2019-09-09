---
UID: NF:d2d1.ID2D1RenderTarget.SetTransform(const D2D1_MATRIX_3X2_F)
title: ID2D1RenderTarget::SetTransform (d2d1.h)
author: windows-sdk-content
description: Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.
old-location: direct2d\ID2D1RenderTarget_SetTransform_ptr_D2D_MATRIX_3X2_F.htm
tech.root: Direct2D
ms.assetid: c358ea97-c42e-4912-a4e4-9a30935bd95b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetTransform method, ID2D1RenderTarget.SetTransform, ID2D1RenderTarget::SetTransform, ID2D1RenderTarget::SetTransform(const D2D1_MATRIX_3X2_F), SetTransform, SetTransform method [Direct2D], SetTransform method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetTransform, direct2d.ID2D1RenderTarget_SetTransform_ptr_D2D_MATRIX_3X2_F
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget.SetTransform"
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
 - ID2D1RenderTarget.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::SetTransform


## -description


Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.


## -parameters




### -param transform [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the render target.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-apply-multiple-transforms">How to Apply Multiple Transforms to an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-rotate">How to Rotate an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-scale">How to Scale an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-skew">How to Skew an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-translate">How to Translate an Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-transforms-overview">Transforms Overview</a>
 

 

