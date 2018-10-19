---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetGradientStops1
title: ID2D1GradientStopCollection1::GetGradientStops1
author: windows-sdk-content
description: Copies the gradient stops from the collection into memory.
old-location: direct2d\id2d1gradientstopcollection1_getgradientstops1.htm
tech.root: direct2d
ms.assetid: da3987a5-b40f-49eb-9930-0162cf64d6a9
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetGradientStops1, GetGradientStops1 method [Direct2D], GetGradientStops1 method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetGradientStops1 method, ID2D1GradientStopCollection1.GetGradientStops1, ID2D1GradientStopCollection1::GetGradientStops1, d2d1_1/ID2D1GradientStopCollection1::GetGradientStops1, direct2d.id2d1gradientstopcollection1_getgradientstops1
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
 - ID2D1GradientStopCollection1.GetGradientStops1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientStopCollection1::GetGradientStops1


## -description


Copies the gradient stops from the collection into memory.


## -parameters




### -param gradientStops [out]

Type: <b><a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>*</b>

When this method returns, contains a pointer to a one-dimensional array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures.


### -param gradientStopsCount

Type: <b>UINT</b>

The number of gradient stops to copy. 


## -returns



This method does not return a value.




## -remarks



If the <a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a> object was created using <a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1DeviceContext::CreateGradientStopCollection</a>, this method returns the same values specified in the creation method. If the <b>ID2D1GradientStopCollection1</b> object was created using <b>ID2D1RenderTarget::CreateGradientStopCollection</b>, the stops returned here will first be transformed into the gamma space specified by the <i>colorInterpolationGamma</i> parameter. See the <a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">ID2D1DeviceContext::CreateGradientStopCollection</a>  method for more info about color space and gamma space.

If <i>gradientStopsCount</i> is less than the number of gradient stops in the collection, the remaining gradient stops are omitted. If <i>gradientStopsCount</i> is larger than the number of gradient stops in the collection, the extra gradient stops are set to <b>NULL</b>. To obtain the number of gradient stops in the collection, use the <a href="https://msdn.microsoft.com/1c3ef4b0-e781-4177-81a4-b39add8468a0">GetGradientStopCount</a> method.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

