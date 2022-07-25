---
UID: NF:dwrite.IDWriteTextLayout.Draw
title: IDWriteTextLayout::Draw (dwrite.h)
description: Draws text using the specified client drawing context.
helpviewer_keywords: ["Draw","Draw method [Direct Write]","Draw method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","Draw method","IDWriteTextLayout.Draw","IDWriteTextLayout::Draw","directwrite.IDWriteTextLayout_Draw","dwrite/IDWriteTextLayout::Draw"]
old-location: directwrite\IDWriteTextLayout_Draw.htm
tech.root: DirectWrite
ms.assetid: 8d92a7c3-4804-47f6-bfca-5322be119cbb
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Direct Write], Draw method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],Draw method, IDWriteTextLayout.Draw, IDWriteTextLayout::Draw, directwrite.IDWriteTextLayout_Draw, dwrite/IDWriteTextLayout::Draw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextLayout::Draw
 - dwrite/IDWriteTextLayout::Draw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout.Draw
---

# IDWriteTextLayout::Draw


## -description

 Draws text using the specified client drawing context.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

An application-defined drawing context.

### -param renderer

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a>*</b>

Pointer to the set of callback functions used to draw parts of a text string.

### -param originX

Type: <b>FLOAT</b>

The x-coordinate of the layout's left side.

### -param originY

Type: <b>FLOAT</b>

The y-coordinate of the layout's top side.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To draw text with this method, a <i>textLayout</i> object needs to be created by the application using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">IDWriteFactory::CreateTextLayout</a>. 

After the <i>textLayout</i> object is obtained, the application calls the  <b>IDWriteTextLayout::Draw</b> method  to draw the text, decorations, and inline objects. The actual drawing is done through the callback interface passed in as the <i>textRenderer</i> argument; there, the corresponding <a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun">DrawGlyphRun</a> API is called. 

If you set a vertical text reading direction on IDWriteTextLayout via SetReadingDirection with DWRITE_READING_DIRECTION_TOP_TO_BOTTOM (or bottom to top), then you must pass an interface that implements IDWriteTextRenderer1. Otherwise you get the error DWRITE_E_TEXTRENDERERINCOMPATIBLE because the original IDWriteTextRenderer interface only supported horizontal text.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

