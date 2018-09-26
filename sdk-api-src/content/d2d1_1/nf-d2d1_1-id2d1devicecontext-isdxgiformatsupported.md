---
UID: NF:d2d1_1.ID2D1DeviceContext.IsDxgiFormatSupported
title: ID2D1DeviceContext::IsDxgiFormatSupported
author: windows-sdk-content
description: Indicates whether the format is supported by the device context.
old-location: direct2d\id2d1devicecontext_isdxgiformatsupported.htm
tech.root: direct2d
ms.assetid: AA70292A-7B1C-4916-91CA-80263839BC3F
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],IsDxgiFormatSupported method, ID2D1DeviceContext.IsDxgiFormatSupported, ID2D1DeviceContext::IsDxgiFormatSupported, IsDxgiFormatSupported, IsDxgiFormatSupported method [Direct2D], IsDxgiFormatSupported method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::IsDxgiFormatSupported, direct2d.id2d1devicecontext_isdxgiformatsupported
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
 - ID2D1DeviceContext.IsDxgiFormatSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::IsDxgiFormatSupported


## -description


 Indicates whether the format is supported by the device context.  The formats supported are usually determined by the underlying hardware.


## -parameters




### -param format

TBD




#### - DXGI_FORMAT

Type: <b>format</b>

The DXGI format to check.


## -returns



Type: <b>BOOL</b>

Returns TRUE if the format is supported.  Returns FALSE if the format is not supported.




## -remarks



You can use supported formats in the <a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a> structure to create bitmaps and render targets.

Direct2D doesn't support all DXGI formats, even though they may have some level of Direct3D support by the hardware.





## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

