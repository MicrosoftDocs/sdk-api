---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetPreInterpolationSpace
title: ID2D1GradientStopCollection1::GetPreInterpolationSpace
author: windows-sdk-content
description: Gets the color space of the input colors as well as the space in which gradient stops are interpolated.
old-location: direct2d\id2d1gradientstopcollection1_getpreinterpolationspace.htm
tech.root: direct2d
ms.assetid: 8222d713-c47e-4e4c-92aa-040dc9085ce9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetPreInterpolationSpace, GetPreInterpolationSpace method [Direct2D], GetPreInterpolationSpace method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetPreInterpolationSpace method, ID2D1GradientStopCollection1.GetPreInterpolationSpace, ID2D1GradientStopCollection1::GetPreInterpolationSpace, d2d1_1/ID2D1GradientStopCollection1::GetPreInterpolationSpace, direct2d.id2d1gradientstopcollection1_getpreinterpolationspace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1GradientStopCollection1.GetPreInterpolationSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientStopCollection1::GetPreInterpolationSpace


## -description


Gets the color space of the input colors as well as the space in which gradient stops are interpolated.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

This method returns the color space.




## -remarks



If this object was created using <a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>, this method  returns the color space related to the color interpolation gamma.
 




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

