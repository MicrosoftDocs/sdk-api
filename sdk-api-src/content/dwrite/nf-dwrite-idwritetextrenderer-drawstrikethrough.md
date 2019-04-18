---
UID: NF:dwrite.IDWriteTextRenderer.DrawStrikethrough
title: IDWriteTextRenderer::DrawStrikethrough (dwrite.h)
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw a strikethrough.
old-location: directwrite\IDWriteTextRenderer_DrawStrikethrough.htm
tech.root: DirectWrite
ms.assetid: d7888c99-ff7c-4e14-b0a6-4726c9228226
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawStrikethrough, DrawStrikethrough method [Direct Write], DrawStrikethrough method [Direct Write],IDWriteTextRenderer interface, IDWriteTextRenderer interface [Direct Write],DrawStrikethrough method, IDWriteTextRenderer.DrawStrikethrough, IDWriteTextRenderer::DrawStrikethrough, directwrite.IDWriteTextRenderer_DrawStrikethrough, dwrite/IDWriteTextRenderer::DrawStrikethrough
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
 - IDWriteTextRenderer.DrawStrikethrough
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextRenderer::DrawStrikethrough


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




<a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>
 

 

