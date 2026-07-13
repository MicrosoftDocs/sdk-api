---
UID: NF:dwrite_3.IDWriteFontFamily1.GetFont
title: IDWriteFontFamily1::GetFont (dwrite_3.h)
description: Gets a font given its zero-based index. (IDWriteFontFamily1.GetFont)
helpviewer_keywords: ["GetFont","GetFont method [Direct Write]","GetFont method [Direct Write]","IDWriteFontFamily1 interface","IDWriteFontFamily1 interface [Direct Write]","GetFont method","IDWriteFontFamily1.GetFont","IDWriteFontFamily1::GetFont","directwrite.idwritefontfamily1_getfont","dwrite_3/IDWriteFontFamily1::GetFont"]
old-location: directwrite\idwritefontfamily1_getfont.htm
tech.root: DirectWrite
ms.assetid: B5C03AC5-E642-4AC8-94D1-D935BA159113
ms.date: 09/10/2025
ms.keywords: GetFont, GetFont method [Direct Write], GetFont method [Direct Write],IDWriteFontFamily1 interface, IDWriteFontFamily1 interface [Direct Write],GetFont method, IDWriteFontFamily1.GetFont, IDWriteFontFamily1::GetFont, directwrite.idwritefontfamily1_getfont, dwrite_3/IDWriteFontFamily1::GetFont
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFamily1::GetFont
 - dwrite_3/IDWriteFontFamily1::GetFont
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
 - IDWriteFontFamily1.GetFont
---

# IDWriteFontFamily1::GetFont


## -description

Gets a font given its zero-based index.

## -parameters

### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.

### -param font [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a> interface for the newly created font object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1">IDWriteFontFamily1</a>

