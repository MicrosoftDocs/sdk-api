---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F)
title: ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F)
author: windows-sdk-content
description: Draw a metafile to the device context.
old-location: direct2d\id2d1devicecontext_drawgdimetafile.htm
tech.root: direct2d
ms.assetid: d0746d7f-0779-46c0-8a02-c92e6851e371
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawGdiMetafile method, ID2D1DeviceContext.DrawGdiMetafile, ID2D1DeviceContext.DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F), ID2D1DeviceContext::DrawGdiMetafile, ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F), d2d1_1/ID2D1DeviceContext::DrawGdiMetafile, direct2d.id2d1devicecontext_drawgdimetafile
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
 - ID2D1DeviceContext.DrawGdiMetafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F)


## -description


Draw a metafile to the device context.


## -parameters




### -param gdiMetafile [in]

Type: <b><a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a>*</b>

The metafile to draw.


### -param targetOffset [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The offset from the upper left corner of the render target.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

