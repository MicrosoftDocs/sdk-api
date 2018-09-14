---
UID: NF:d2d1_1.ID2D1DeviceContext.IsBufferPrecisionSupported
title: ID2D1DeviceContext::IsBufferPrecisionSupported
author: windows-sdk-content
description: Indicates whether the buffer precision is supported by the underlying Direct3D device.
old-location: direct2d\id2d1devicecontext_isbufferprecisionsupported.htm
tech.root: Direct2D
ms.assetid: c65824dc-a9d5-4d4d-a2de-b4283153f64f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],IsBufferPrecisionSupported method, ID2D1DeviceContext.IsBufferPrecisionSupported, ID2D1DeviceContext::IsBufferPrecisionSupported, IsBufferPrecisionSupported, IsBufferPrecisionSupported method [Direct2D], IsBufferPrecisionSupported method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::IsBufferPrecisionSupported, direct2d.id2d1devicecontext_isbufferprecisionsupported
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
 - ID2D1DeviceContext.IsBufferPrecisionSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::IsBufferPrecisionSupported


## -description


Indicates whether the buffer precision is supported by the underlying Direct3D <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">device.</a>



## -parameters




### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The buffer precision to check.


## -returns



Type: <b>BOOL</b>

Returns TRUE if the buffer precision is supported.  Returns FALSE if the buffer precision is not supported.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

