---
UID: NF:dwrite_3.IDWriteTextFormat2.GetLineSpacing
title: IDWriteTextFormat2::GetLineSpacing (dwrite_3.h)
description: Gets the line spacing adjustment set for a multiline text paragraph. (IDWriteTextFormat2.GetLineSpacing)
helpviewer_keywords: ["GetLineSpacing","GetLineSpacing method [Direct Write]","GetLineSpacing method [Direct Write]","IDWriteTextFormat2 interface","IDWriteTextFormat2 interface [Direct Write]","GetLineSpacing method","IDWriteTextFormat2.GetLineSpacing","IDWriteTextFormat2::GetLineSpacing","directwrite.idwritetextformat2_getlinespacing","dwrite_3/IDWriteTextFormat2::GetLineSpacing"]
old-location: directwrite\idwritetextformat2_getlinespacing.htm
tech.root: DirectWrite
ms.assetid: 1e05687f-137e-06f8-b9c8-983f434f7578
ms.date: 09/10/2025
ms.keywords: GetLineSpacing, GetLineSpacing method [Direct Write], GetLineSpacing method [Direct Write],IDWriteTextFormat2 interface, IDWriteTextFormat2 interface [Direct Write],GetLineSpacing method, IDWriteTextFormat2.GetLineSpacing, IDWriteTextFormat2::GetLineSpacing, directwrite.idwritetextformat2_getlinespacing, dwrite_3/IDWriteTextFormat2::GetLineSpacing
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteTextFormat2::GetLineSpacing
 - dwrite_3/IDWriteTextFormat2::GetLineSpacing
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
 - IDWriteTextFormat2.GetLineSpacing
---

# IDWriteTextFormat2::GetLineSpacing


## -description

Gets the line spacing adjustment set for a multiline text paragraph.

## -parameters

### -param lineSpacingOptions [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing">DWRITE_LINE_SPACING</a>*</b>

A structure describing how the space between lines is managed for the paragraph.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat2">IDWriteTextFormat2</a>

