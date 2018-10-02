---
UID: NF:d2d1_1.ID2D1CommandSink.FillOpacityMask
title: ID2D1CommandSink::FillOpacityMask
author: windows-sdk-content
description: Fills an opacity mask on the command sink.
old-location: direct2d\id2d1commandsink_fillopacitymask.htm
tech.root: direct2d
ms.assetid: c125b2db-0786-4bda-b31f-de05ba72afa1
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillOpacityMask method, ID2D1CommandSink.FillOpacityMask, ID2D1CommandSink::FillOpacityMask, d2d1_1/ID2D1CommandSink::FillOpacityMask, direct2d.id2d1commandsink_fillopacitymask
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
 - ID2D1CommandSink.FillOpacityMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::FillOpacityMask


## -description


Fills an opacity mask on the command sink.


## -parameters




### -param opacityMask [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap whose alpha channel will be sampled to define the opacity mask.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush with which to fill the mask.


### -param destinationRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The destination rectangle in which to fill the mask. If not specified, this is the origin.


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The source rectangle within the opacity mask. If not specified, this is the entire mask.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



The opacity mask bitmap must be considered to be clamped on each axis.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/a5e56d8a-2929-4f7b-b1c4-fb358c202721">ID2D1RenderTarget::FillOpacityMask</a>
 

 

