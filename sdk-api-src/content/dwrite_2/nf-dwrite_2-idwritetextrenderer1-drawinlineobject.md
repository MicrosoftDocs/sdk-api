---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawInlineObject
title: IDWriteTextRenderer1::DrawInlineObject
author: windows-sdk-content
description: IDWriteTextLayout::Draw calls this application callback when it needs to draw an inline object.
old-location: directwrite\idwritetextrenderer1_drawinlineobject.htm
tech.root: DirectWrite
ms.assetid: 1115e215-d04e-28db-c196-7d693ca91044
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawInlineObject, DrawInlineObject method [Direct Write], DrawInlineObject method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawInlineObject method, IDWriteTextRenderer1.DrawInlineObject, IDWriteTextRenderer1::DrawInlineObject, directwrite.idwritetextrenderer1_drawinlineobject, dwrite_2/IDWriteTextRenderer1::DrawInlineObject
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
 - IDWriteTextRenderer1.DrawInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer1::DrawInlineObject


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


### -param orientationAngle

Type: <b><a href="https://msdn.microsoft.com/BD9D0C11-B286-4E4A-B641-1DB9F75803B0">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the inline object.


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




<a href="https://msdn.microsoft.com/A8C39C54-AF98-4A27-9BCF-9C132F4CD3B1">IDWriteTextRenderer1</a>
 

 

