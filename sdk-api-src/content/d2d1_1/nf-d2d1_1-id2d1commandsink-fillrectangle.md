---
UID: NF:d2d1_1.ID2D1CommandSink.FillRectangle
title: ID2D1CommandSink::FillRectangle
author: windows-sdk-content
description: Indicates to the command sink a rectangle to be filled.
old-location: direct2d\id2d1commandsink_fillrectangle.htm
tech.root: direct2d
ms.assetid: c970a962-8d03-4de8-9252-9babfa411e5f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FillRectangle, FillRectangle method [Direct2D], FillRectangle method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillRectangle method, ID2D1CommandSink.FillRectangle, ID2D1CommandSink::FillRectangle, d2d1_1/ID2D1CommandSink::FillRectangle, direct2d.id2d1commandsink_fillrectangle
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
 - ID2D1CommandSink.FillRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::FillRectangle


## -description


Indicates to the command sink a rectangle to be filled.


## -parameters




### -param rect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle to fill.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush with which to fill the rectangle.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/08e498f9-b564-4da6-ba9b-bff08964ce08">ID2D1RenderTarget::FillRectangle</a>
 

 

