---
UID: NF:d2d1_1.ID2D1CommandSink.DrawLine
title: ID2D1CommandSink::DrawLine
author: windows-sdk-content
description: Draws a line drawn between two points.
old-location: direct2d\id2d1commandsink_drawline.htm
tech.root: Direct2D
ms.assetid: 3c47b5af-d258-42f8-b329-eb28d9485d3a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrawLine, DrawLine method [Direct2D], DrawLine method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawLine method, ID2D1CommandSink.DrawLine, ID2D1CommandSink::DrawLine, d2d1_1/ID2D1CommandSink::DrawLine, direct2d.id2d1commandsink_drawline
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
 - ID2D1CommandSink.DrawLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawLine


## -description


Draws a line drawn between two points.


## -parameters




### -param point0

TBD


### -param point1

TBD


### -param brush

TBD


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke to fill the line.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of the stroke. If not specified, the stroke is solid.


#### - Brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to fill the line.


#### - Point0

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The start point of the line.


#### - Point1

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point of the line.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/7eb70308-4142-4d32-a070-9e937579b896">ID2D1RenderTarget::DrawLine</a>
 

 

