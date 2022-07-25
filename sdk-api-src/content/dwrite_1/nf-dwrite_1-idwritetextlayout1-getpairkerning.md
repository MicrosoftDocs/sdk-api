---
UID: NF:dwrite_1.IDWriteTextLayout1.GetPairKerning
title: IDWriteTextLayout1::GetPairKerning (dwrite_1.h)
description: Gets whether or not pair-kerning is enabled at given position.
helpviewer_keywords: ["GetPairKerning","GetPairKerning method [Direct Write]","GetPairKerning method [Direct Write]","IDWriteTextLayout1 interface","IDWriteTextLayout1 interface [Direct Write]","GetPairKerning method","IDWriteTextLayout1.GetPairKerning","IDWriteTextLayout1::GetPairKerning","directwrite.idwritetextlayout1_getpairkerning","dwrite_1/IDWriteTextLayout1::GetPairKerning"]
old-location: directwrite\idwritetextlayout1_getpairkerning.htm
tech.root: DirectWrite
ms.assetid: 24E89191-E543-4AF4-A8F5-10CB4B0AF6B0
ms.date: 12/05/2018
ms.keywords: GetPairKerning, GetPairKerning method [Direct Write], GetPairKerning method [Direct Write],IDWriteTextLayout1 interface, IDWriteTextLayout1 interface [Direct Write],GetPairKerning method, IDWriteTextLayout1.GetPairKerning, IDWriteTextLayout1::GetPairKerning, directwrite.idwritetextlayout1_getpairkerning, dwrite_1/IDWriteTextLayout1::GetPairKerning
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextLayout1::GetPairKerning
 - dwrite_1/IDWriteTextLayout1::GetPairKerning
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
 - IDWriteTextLayout1.GetPairKerning
---

# IDWriteTextLayout1::GetPairKerning


## -description

Gets whether or not pair-kerning is enabled at given position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The current text position.

### -param isPairKerningEnabled [out]

Type: <b>BOOL*</b>

The flag that indicates whether text is pair-kerned.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The position range of the current format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>

