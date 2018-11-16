---
UID: NF:dwrite.IDWriteTextRenderer.DrawUnderline
title: IDWriteTextRenderer::DrawUnderline
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw an underline.
old-location: directwrite\IDWriteTextRenderer_DrawUnderline.htm
tech.root: DirectWrite
ms.assetid: 23395b2a-f53c-4697-87f1-15c65224b1f3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrawUnderline, DrawUnderline method [Direct Write], DrawUnderline method [Direct Write],IDWriteTextRenderer interface, IDWriteTextRenderer interface [Direct Write],DrawUnderline method, IDWriteTextRenderer.DrawUnderline, IDWriteTextRenderer::DrawUnderline, directwrite.IDWriteTextRenderer_DrawUnderline, dwrite/IDWriteTextRenderer::DrawUnderline
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextRenderer.DrawUnderline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteTextRenderer.DrawUnderline
: 
---

# IDWriteTextRenderer::DrawUnderline


## -description


 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     an underline.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a>.


### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the run where underline applies.


### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the run where underline applies.


### -param underline [in]

Type: <b>const <a href="https://msdn.microsoft.com/01f6c48e-6986-4a6e-9dd8-9f4b098db7fd">DWRITE_UNDERLINE</a>*</b>

Pointer to  a structure containing underline logical information.


### -param clientDrawingEffect

Type: <b>IUnknown*</b>

 Application-defined effect to apply to the underline. Usually this argument represents effects such as the foreground brush filling the interior of a line.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 A single underline can be broken into multiple calls, depending on
     how the formatting changes attributes. If font sizes/styles change
     within an underline, the thickness and offset will be averaged
     weighted according to characters.
     To get an appropriate starting pixel position, add underline::offset
     to the baseline. Otherwise there will be no spacing between the text.
     The x coordinate will always be passed as the left side, regardless
     of text directionality. This simplifies drawing and reduces the
     problem of round-off that could potentially cause gaps or a double
     stamped alpha blend. To avoid alpha overlap, round the end points
     to the nearest device pixel.




## -see-also




<a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>
 

 

