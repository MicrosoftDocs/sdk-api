---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F)
title: ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F) (d2d1_1.h)
author: windows-sdk-content
description: Draw a metafile to the device context.
old-location: direct2d\id2d1devicecontext_drawgdimetafile.htm
tech.root: Direct2D
ms.assetid: d0746d7f-0779-46c0-8a02-c92e6851e371
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawGdiMetafile method, ID2D1DeviceContext.DrawGdiMetafile, ID2D1DeviceContext.DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F), ID2D1DeviceContext::DrawGdiMetafile, ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F), d2d1_1/ID2D1DeviceContext::DrawGdiMetafile, direct2d.id2d1devicecontext_drawgdimetafile
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
ms.custom: 19H1
---

# ID2D1DeviceContext::DrawGdiMetafile(ID2D1GdiMetafile,D2D1_POINT_2F)


## -description


Draw a metafile to the device context.


## -parameters




### -param gdiMetafile [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>*</b>

The metafile to draw.


### -param targetOffset [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

The offset from the upper left corner of the render target.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
 

 

