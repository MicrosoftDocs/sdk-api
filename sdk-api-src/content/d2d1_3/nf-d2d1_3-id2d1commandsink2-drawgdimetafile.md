---
UID: NF:d2d1_3.ID2D1CommandSink2.DrawGdiMetafile
title: ID2D1CommandSink2::DrawGdiMetafile
author: windows-sdk-content
description: Draws a metafile to the command sink using the given source and destination rectangles.
old-location: direct2d\id2d1commandsink2_drawgdimetafile.htm
tech.root: direct2d
ms.assetid: ecd1fb9e-0062-c1aa-8275-47b7453bc9ad
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1CommandSink2 interface, ID2D1CommandSink2 interface [Direct2D],DrawGdiMetafile method, ID2D1CommandSink2.DrawGdiMetafile, ID2D1CommandSink2::DrawGdiMetafile, d2d1_3/ID2D1CommandSink2::DrawGdiMetafile, direct2d.id2d1commandsink2_drawgdimetafile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID2D1CommandSink2.DrawGdiMetafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink2::DrawGdiMetafile


## -description


Draws a metafile to the command sink using the given source and destination rectangles.


## -parameters




### -param gdiMetafile [in]

Type: <b><a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a>*</b>

The metafile to draw.


### -param destinationRectangle [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle in the target where the metafile will be drawn, relative to the upper left corner (defined in DIPs). If NULL is specified, the destination rectangle is the size of the target.


### -param sourceRectangle [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle of the source metafile that will be drawn, relative to the upper left corner (defined in DIPs). 
     If NULL is specified, the source rectangle is the value returned by <a href="https://msdn.microsoft.com/7e7502ee-678e-ce26-cc0b-266faa1c320b">ID2D1GdiMetafile1::GetSourceBounds</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/bd1a22a8-bbf3-d515-5596-1797e261cd1e">ID2D1CommandSink2</a>
 

 

