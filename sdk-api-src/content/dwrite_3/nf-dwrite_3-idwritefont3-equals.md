---
UID: NF:dwrite_3.IDWriteFont3.Equals
title: IDWriteFont3::Equals (dwrite_3.h)
description: Compares two instances of font references for equality.
helpviewer_keywords: ["Equals","Equals method [Direct Write]","Equals method [Direct Write]","IDWriteFont3 interface","IDWriteFont3 interface [Direct Write]","Equals method","IDWriteFont3.Equals","IDWriteFont3::Equals","directwrite.idwritefont3_equals","dwrite_3/IDWriteFont3::Equals"]
old-location: directwrite\idwritefont3_equals.htm
tech.root: DirectWrite
ms.assetid: 4C537868-F655-457F-9B70-FA7633CF714C
ms.date: 09/10/2025
ms.keywords: Equals, Equals method [Direct Write], Equals method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],Equals method, IDWriteFont3.Equals, IDWriteFont3::Equals, directwrite.idwritefont3_equals, dwrite_3/IDWriteFont3::Equals
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
 - IDWriteFont3::Equals
 - dwrite_3/IDWriteFont3::Equals
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
 - IDWriteFont3.Equals
---

# IDWriteFont3::Equals


## -description

Compares two instances of font references for equality.

## -parameters

### -param font [in]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a> interface for the other font instance to compare to this font instance.

## -returns

Type: <b>BOOL</b>

Returns whether the two instances of font references are equal. Returns <b>TRUE</b> if the two instances are equal; otherwise, <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>

