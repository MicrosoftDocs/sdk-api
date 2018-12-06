---
UID: NF:d2d1_3.ID2D1DeviceContext2.DrawGdiMetafile(ID2D1GdiMetafile,const D2D1_RECT_F &,const D2D1_RECT_F)
title: ID2D1DeviceContext2::DrawGdiMetafile(ID2D1GdiMetafile,const D2D1_RECT_F &,const D2D1_RECT_F)
author: windows-sdk-content
description: Draws a metafile to the device context using the given source and destination rectangles.
old-location: direct2d\id2d1devicecontext2_drawgdimetafile3.htm
tech.root: direct2d
ms.assetid: 05de3273-7313-ff52-39bb-376661b9c283
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawGdiMetafile, DrawGdiMetafile method [Direct2D], DrawGdiMetafile method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],DrawGdiMetafile method, ID2D1DeviceContext2.DrawGdiMetafile, ID2D1DeviceContext2.DrawGdiMetafile(ID2D1GdiMetafile,const D2D1_RECT_F &,const D2D1_RECT_F), ID2D1DeviceContext2::DrawGdiMetafile, ID2D1DeviceContext2::DrawGdiMetafile(ID2D1GdiMetafile,const D2D1_RECT_F &,const D2D1_RECT_F), d2d1_3/ID2D1DeviceContext2::DrawGdiMetafile, direct2d.id2d1devicecontext2_drawgdimetafile3
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
 - ID2D1DeviceContext2.DrawGdiMetafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::DrawGdiMetafile(ID2D1GdiMetafile,const D2D1_RECT_F &,const D2D1_RECT_F)


## -description


Draws a metafile to the device context using the given source and destination rectangles.


## -parameters




### -param gdiMetafile [in]

Type: <b><a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a>*</b>

The metafile to draw.


### -param destinationRectangle [ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle in the target where the metafile will be drawn, relative to the upper left corner (defined in DIPs) of the render target. 
     If NULL is specified, the destination rectangle is {0, 0, w, h}, where w and h are the width and height of the metafile as reported by <a href="https://msdn.microsoft.com/59DA5314-2A6C-42B0-A4B8-72F6302B4B0F">ID2D1GdiMetafile::GetBounds</a>. 


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle of the source metafile that will be drawn, relative to the upper left corner (defined in DIPs) of the metafile. 
     If NULL is specified, the source rectangle is the value returned by <a href="https://msdn.microsoft.com/7e7502ee-678e-ce26-cc0b-266faa1c320b">ID2D1GdiMetafile1::GetSourceBounds</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

