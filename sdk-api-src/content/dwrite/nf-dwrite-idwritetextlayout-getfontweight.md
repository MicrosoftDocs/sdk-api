---
UID: NF:dwrite.IDWriteTextLayout.GetFontWeight
title: IDWriteTextLayout::GetFontWeight (dwrite.h)
description: Gets the font weight of the text at the specified position.
helpviewer_keywords: ["GetFontWeight","GetFontWeight method [Direct Write]","GetFontWeight method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontWeight method","IDWriteTextLayout.GetFontWeight","IDWriteTextLayout::GetFontWeight","directwrite.IDWriteTextLayout_GetFontWeight","dwrite/IDWriteTextLayout::GetFontWeight"]
old-location: directwrite\IDWriteTextLayout_GetFontWeight.htm
tech.root: DirectWrite
ms.assetid: e1c86c8e-f6d2-4c72-9117-f8ae4334a71b
ms.date: 12/05/2018
ms.keywords: GetFontWeight, GetFontWeight method [Direct Write], GetFontWeight method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontWeight method, IDWriteTextLayout.GetFontWeight, IDWriteTextLayout::GetFontWeight, directwrite.IDWriteTextLayout_GetFontWeight, dwrite/IDWriteTextLayout::GetFontWeight
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
 - IDWriteTextLayout::GetFontWeight
 - dwrite/IDWriteTextLayout::GetFontWeight
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
 - IDWriteTextLayout.GetFontWeight
---

# IDWriteTextLayout::GetFontWeight


## -description

Gets the font weight of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param fontWeight [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a>*</b>

When this method returns, contains a value which indicates the type of font weight being applied at the specified position.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font weight.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

