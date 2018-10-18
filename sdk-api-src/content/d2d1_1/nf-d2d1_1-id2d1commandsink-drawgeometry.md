---
UID: NF:d2d1_1.ID2D1CommandSink.DrawGeometry
title: ID2D1CommandSink::DrawGeometry
author: windows-sdk-content
description: Indicates the geometry to be drawn to the command sink.
old-location: direct2d\id2d1commandsink_drawgeometry.htm
tech.root: direct2d
ms.assetid: ff91dd6c-0604-44aa-a30c-6b531cc3fb58
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: DrawGeometry, DrawGeometry method [Direct2D], DrawGeometry method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawGeometry method, ID2D1CommandSink.DrawGeometry, ID2D1CommandSink::DrawGeometry, d2d1_1/ID2D1CommandSink::DrawGeometry, direct2d.id2d1commandsink_drawgeometry
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
 - ID2D1CommandSink.DrawGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawGeometry


## -description


Indicates the geometry to be drawn to the command sink.


## -parameters




### -param geometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry </a>*</b>

The geometry to be stroked.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush that will be used to fill the stroked geometry.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of the stroke.


## -returns



Type: <b>HRESULT</b>

An HRESULT. 




## -remarks




<a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">Ellipses</a> and <a href="https://msdn.microsoft.com/e49e9be7-155a-4487-9931-035f18771c04">rounded rectangles</a> are converted to the corresponding ellipse and rounded rectangle geometries before calling into the <b>DrawGeometry</b> method.





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/319b2680-34f8-4e00-985e-47ff87115794">ID2D1RenderTarget::DrawGeometry</a>
 

 

