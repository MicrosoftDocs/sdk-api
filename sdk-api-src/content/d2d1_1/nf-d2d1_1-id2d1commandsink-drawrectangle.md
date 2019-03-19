---
UID: NF:d2d1_1.ID2D1CommandSink.DrawRectangle
title: ID2D1CommandSink::DrawRectangle (d2d1_1.h)
author: windows-sdk-content
description: Draws a rectangle.
old-location: direct2d\id2d1commandsink_drawrectangle.htm
tech.root: Direct2D
ms.assetid: 93c617fb-3c9d-4735-a077-7a3a58033369
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawRectangle, DrawRectangle method [Direct2D], DrawRectangle method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawRectangle method, ID2D1CommandSink.DrawRectangle, ID2D1CommandSink::DrawRectangle, d2d1_1/ID2D1CommandSink::DrawRectangle, direct2d.id2d1commandsink_drawrectangle
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
 - ID2D1CommandSink.DrawRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawRectangle


## -description


Draws a rectangle.


## -parameters




### -param rect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle to be drawn to the command sink.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to stroke the geometry.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of the stroke.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742846(v=VS.85).aspx">ID2D1RenderTarget::DrawRectangle</a>
 

 

