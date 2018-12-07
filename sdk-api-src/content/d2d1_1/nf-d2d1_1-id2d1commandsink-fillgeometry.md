---
UID: NF:d2d1_1.ID2D1CommandSink.FillGeometry
title: ID2D1CommandSink::FillGeometry
author: windows-sdk-content
description: Indicates to the command sink a geometry to be filled.
old-location: direct2d\id2d1commandsink_fillgeometry.htm
tech.root: direct2d
ms.assetid: 04e93b19-f3a7-4196-bce0-e656d48116ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FillGeometry, FillGeometry method [Direct2D], FillGeometry method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillGeometry method, ID2D1CommandSink.FillGeometry, ID2D1CommandSink::FillGeometry, d2d1_1/ID2D1CommandSink::FillGeometry, direct2d.id2d1commandsink_fillgeometry
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
 - ID2D1CommandSink.FillGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::FillGeometry


## -description


Indicates to the command sink a geometry to be filled.


## -parameters




### -param geometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry that should be filled.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The primary brush used to fill the geometry.


### -param opacityBrush [in, optional]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

A brush whose alpha channel is used to modify the opacity of the primary fill brush.  


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



If the opacity brush is specified, the primary brush will be a bitmap brush fixed on both the x-axis and the y-axis.

Ellipses and rounded rectangles are converted to the corresponding geometry before being passed to <b>FillGeometry</b>.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">ID2D1RenderTarget::FillGeometry</a>
 

 

