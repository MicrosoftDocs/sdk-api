---
UID: NF:dwrite_1.IDWriteTextLayout1.SetPairKerning
title: IDWriteTextLayout1::SetPairKerning (dwrite_1.h)
description: Enables or disables pair-kerning on a given text range.
helpviewer_keywords: ["IDWriteTextLayout1 interface [Direct Write]","SetPairKerning method","IDWriteTextLayout1.SetPairKerning","IDWriteTextLayout1::SetPairKerning","SetPairKerning","SetPairKerning method [Direct Write]","SetPairKerning method [Direct Write]","IDWriteTextLayout1 interface","directwrite.idwritetextlayout1_setpairkerning","dwrite_1/IDWriteTextLayout1::SetPairKerning"]
old-location: directwrite\idwritetextlayout1_setpairkerning.htm
tech.root: DirectWrite
ms.assetid: AE43D7E4-CD2D-4BBD-88C3-B5287FD235AF
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout1 interface [Direct Write],SetPairKerning method, IDWriteTextLayout1.SetPairKerning, IDWriteTextLayout1::SetPairKerning, SetPairKerning, SetPairKerning method [Direct Write], SetPairKerning method [Direct Write],IDWriteTextLayout1 interface, directwrite.idwritetextlayout1_setpairkerning, dwrite_1/IDWriteTextLayout1::SetPairKerning
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
 - IDWriteTextLayout1::SetPairKerning
 - dwrite_1/IDWriteTextLayout1::SetPairKerning
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
 - IDWriteTextLayout1.SetPairKerning
---

# IDWriteTextLayout1::SetPairKerning


## -description

Enables or disables pair-kerning on a given text range.

## -parameters

### -param isPairKerningEnabled

Type: <b>BOOL</b>

The flag that indicates whether text is pair-kerned.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

The text range to which the change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>

