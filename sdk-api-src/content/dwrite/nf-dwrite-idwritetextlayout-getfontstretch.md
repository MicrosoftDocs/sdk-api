---
UID: NF:dwrite.IDWriteTextLayout.GetFontStretch
title: IDWriteTextLayout::GetFontStretch (dwrite.h)
description: Gets the font stretch of the text at the specified position.
helpviewer_keywords: ["GetFontStretch","GetFontStretch method [Direct Write]","GetFontStretch method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontStretch method","IDWriteTextLayout.GetFontStretch","IDWriteTextLayout::GetFontStretch","directwrite.IDWriteTextLayout_GetFontStretch","dwrite/IDWriteTextLayout::GetFontStretch"]
old-location: directwrite\IDWriteTextLayout_GetFontStretch.htm
tech.root: DirectWrite
ms.assetid: f72cdbbf-71ca-45fe-8250-c920c82519e3
ms.date: 12/05/2018
ms.keywords: GetFontStretch, GetFontStretch method [Direct Write], GetFontStretch method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontStretch method, IDWriteTextLayout.GetFontStretch, IDWriteTextLayout::GetFontStretch, directwrite.IDWriteTextLayout_GetFontStretch, dwrite/IDWriteTextLayout::GetFontStretch
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
 - IDWriteTextLayout::GetFontStretch
 - dwrite/IDWriteTextLayout::GetFontStretch
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
 - IDWriteTextLayout.GetFontStretch
---

# IDWriteTextLayout::GetFontStretch


## -description

 Gets the font stretch of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param fontStretch [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch">DWRITE_FONT_STRETCH</a>*</b>

When this method returns, contains a value which indicates the type of font stretch (also known as width) being applied at the specified position.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font stretch.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

