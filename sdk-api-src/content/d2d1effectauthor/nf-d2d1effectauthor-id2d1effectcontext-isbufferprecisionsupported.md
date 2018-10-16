---
UID: NF:d2d1effectauthor.ID2D1EffectContext.IsBufferPrecisionSupported
title: ID2D1EffectContext::IsBufferPrecisionSupported
author: windows-sdk-content
description: Indicates whether the buffer precision is supported by the underlying Direct2D device.
old-location: direct2d\id2d1effectcontext_isbufferprecisionsupported.htm
tech.root: direct2d
ms.assetid: 731A7CF3-03E7-4D38-A8DD-8D207AE90B16
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1EffectContext interface [Direct2D],IsBufferPrecisionSupported method, ID2D1EffectContext.IsBufferPrecisionSupported, ID2D1EffectContext::IsBufferPrecisionSupported, IsBufferPrecisionSupported, IsBufferPrecisionSupported method [Direct2D], IsBufferPrecisionSupported method [Direct2D],ID2D1EffectContext interface, d2d1effectauthor/ID2D1EffectContext::IsBufferPrecisionSupported, direct2d.id2d1effectcontext_isbufferprecisionsupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1EffectContext.IsBufferPrecisionSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::IsBufferPrecisionSupported


## -description


 Indicates whether the buffer precision is supported by the underlying Direct2D <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">device.</a>



## -parameters




### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The buffer precision to check.


## -returns



Type: <b>BOOL</b>

Returns TRUE if the buffer precision is supported.  Returns FALSE if the buffer precision is not supported.




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

