---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetBufferPrecision
title: ID2D1GradientStopCollection1::GetBufferPrecision
author: windows-sdk-content
description: Gets the precision of the gradient buffer.
old-location: direct2d\id2d1gradientstopcollection1_getbufferprecision.htm
tech.root: Direct2D
ms.assetid: 6a59c903-0fa8-4d2c-b426-8d3c3410c6bd
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetBufferPrecision, GetBufferPrecision method [Direct2D], GetBufferPrecision method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetBufferPrecision method, ID2D1GradientStopCollection1.GetBufferPrecision, ID2D1GradientStopCollection1::GetBufferPrecision, d2d1_1/ID2D1GradientStopCollection1::GetBufferPrecision, direct2d.id2d1gradientstopcollection1_getbufferprecision
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
 - ID2D1GradientStopCollection1.GetBufferPrecision
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientStopCollection1::GetBufferPrecision


## -description


Gets the precision of the gradient buffer.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The buffer precision of the gradient buffer.




## -remarks



If this object was created using <a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>, this method returns D2D1_BUFFER_PRECISION_8BPC_UNORM.
  




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

