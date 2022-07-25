---
UID: NF:dwrite.IDWriteTextLayout.GetFontStyle
title: IDWriteTextLayout::GetFontStyle (dwrite.h)
description: Gets the font style (also known as slope) of the text at the specified position.
helpviewer_keywords: ["GetFontStyle","GetFontStyle method [Direct Write]","GetFontStyle method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontStyle method","IDWriteTextLayout.GetFontStyle","IDWriteTextLayout::GetFontStyle","directwrite.IDWriteTextLayout_GetFontStyle","dwrite/IDWriteTextLayout::GetFontStyle"]
old-location: directwrite\IDWriteTextLayout_GetFontStyle.htm
tech.root: DirectWrite
ms.assetid: 184aa6c8-4dc5-4881-a0e0-61dc0b1a8240
ms.date: 12/05/2018
ms.keywords: GetFontStyle, GetFontStyle method [Direct Write], GetFontStyle method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontStyle method, IDWriteTextLayout.GetFontStyle, IDWriteTextLayout::GetFontStyle, directwrite.IDWriteTextLayout_GetFontStyle, dwrite/IDWriteTextLayout::GetFontStyle
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
 - IDWriteTextLayout::GetFontStyle
 - dwrite/IDWriteTextLayout::GetFontStyle
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
 - IDWriteTextLayout.GetFontStyle
---

# IDWriteTextLayout::GetFontStyle


## -description

 Gets the font style (also known as slope) of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param fontStyle [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a>*</b>

When this method returns, contains a value which indicates the type of font style (also known as slope or incline) being applied at the specified position.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font style.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

