---
UID: NF:dwrite.IDWriteTextLayout.SetFontStretch
title: IDWriteTextLayout::SetFontStretch (dwrite.h)
description: Sets the font stretch for text within a specified text range.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetFontStretch method","IDWriteTextLayout.SetFontStretch","IDWriteTextLayout::SetFontStretch","SetFontStretch","SetFontStretch method [Direct Write]","SetFontStretch method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetFontStretch","dwrite/IDWriteTextLayout::SetFontStretch"]
old-location: directwrite\IDWriteTextLayout_SetFontStretch.htm
tech.root: DirectWrite
ms.assetid: 34e7e476-abed-4b0f-a18d-662a277548b1
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontStretch method, IDWriteTextLayout.SetFontStretch, IDWriteTextLayout::SetFontStretch, SetFontStretch, SetFontStretch method [Direct Write], SetFontStretch method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontStretch, dwrite/IDWriteTextLayout::SetFontStretch
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
 - IDWriteTextLayout::SetFontStretch
 - dwrite/IDWriteTextLayout::SetFontStretch
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
 - IDWriteTextLayout.SetFontStretch
---

# IDWriteTextLayout::SetFontStretch


## -description

 Sets the  font stretch for text within a specified text range.

## -parameters

### -param fontStretch

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch">DWRITE_FONT_STRETCH</a></b>

A value which indicates the type of font stretch for text within the range specified by <i>textRange</i>.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

