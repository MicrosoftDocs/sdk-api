---
UID: NF:dwrite.IDWriteTextRenderer.DrawInlineObject
title: IDWriteTextRenderer::DrawInlineObject (dwrite.h)
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this application callback when it needs to draw an inline object.
old-location: directwrite\IDWriteTextRenderer_DrawInlineObject.htm
tech.root: DirectWrite
ms.assetid: ea1c4cd0-d9b5-46af-b53e-a2d8fc442acf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawInlineObject, DrawInlineObject method [Direct Write], DrawInlineObject method [Direct Write],IDWriteTextRenderer interface, IDWriteTextRenderer interface [Direct Write],DrawInlineObject method, IDWriteTextRenderer.DrawInlineObject, IDWriteTextRenderer::DrawInlineObject, directwrite.IDWriteTextRenderer_DrawInlineObject, dwrite/IDWriteTextRenderer::DrawInlineObject
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
 - IDWriteTextRenderer.DrawInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer::DrawInlineObject


## -description


 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this application callback when it needs to
     draw an inline object.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a>.


### -param originX

Type: <b>FLOAT</b>

X-coordinate at the top-left corner of the inline object.


### -param originY

Type: <b>FLOAT</b>

Y-coordinate at the top-left corner of the inline object.


### -param inlineObject

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>*</b>

The application-defined inline object set using <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>::<a href="https://msdn.microsoft.com/19fc9dd8-d732-4078-9db3-bad18681c7ea">SetInlineObject</a>.


### -param isSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object's baseline runs alongside the baseline axis of the line.


### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is in a right-to-left context, hinting that the drawing may want to mirror the normal image.


### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects for the glyphs to render. Usually this argument represents effects such as the foreground brush filling the interior of a line.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>
 

 

