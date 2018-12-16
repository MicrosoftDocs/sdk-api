---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawStrikethrough
title: IDWriteTextRenderer1::DrawStrikethrough
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw a strikethrough.
old-location: directwrite\idwritetextrenderer1_drawstrikethrough.htm
tech.root: DirectWrite
ms.assetid: 8800a536-9477-89c5-c48d-3f4bdf1ca1a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawStrikethrough, DrawStrikethrough method [Direct Write], DrawStrikethrough method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawStrikethrough method, IDWriteTextRenderer1.DrawStrikethrough, IDWriteTextRenderer1::DrawStrikethrough, directwrite.idwritetextrenderer1_drawstrikethrough, dwrite_2/IDWriteTextRenderer1::DrawStrikethrough
ms.topic: method
req.header: dwrite_2.h
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
 - IDWriteTextRenderer1.DrawStrikethrough
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer1::DrawStrikethrough


## -description


 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     a strikethrough.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a>.


### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the run where strikethrough applies.


### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the run where strikethrough applies.


### -param orientationAngle

Type: <b><a href="https://msdn.microsoft.com/BD9D0C11-B286-4E4A-B641-1DB9F75803B0">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the strikethrough.


### -param strikethrough [in]

Type: <b>const <a href="https://msdn.microsoft.com/05d86485-2c34-4e3b-99e8-ca54a3b1e5f6">DWRITE_STRIKETHROUGH</a>*</b>

Pointer to  a structure containing strikethrough logical information.


### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined effect to apply to the strikethrough.  Usually this argument represents effects such as the foreground brush filling the interior of a line.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 A single strikethrough can be broken into multiple calls, depending on
     how the formatting changes attributes. Strikethrough is not averaged
     across font sizes/styles changes.
     To get an appropriate starting pixel position, add strikethrough::offset
     to the baseline.
     Like underlines, the x coordinate will always be passed as the left side,
     regardless of text directionality.




## -see-also




<a href="https://msdn.microsoft.com/A8C39C54-AF98-4A27-9BCF-9C132F4CD3B1">IDWriteTextRenderer1</a>
 

 

