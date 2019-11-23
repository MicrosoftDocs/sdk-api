---
UID: NN:dwrite_3.IDWriteFontFace5
title: IDWriteFontFace5
description: Contains font face type, appropriate file references, and face identification data.

tech.root: DirectWrite

ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5, IDWriteFontFace5 interface [Direct Write], IDWriteFontFace5 interface [Direct Write],described, directwrite.idwritefontface5, dwrite_3/IDWriteFontFace5
ms.topic: interface
f1_keywords:
 - IDWriteFontFace5
dev_langs:
 - c++
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: dwrite_3.h
req.idl: 
req.include-header: 
req.lib: Dwrite.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace5
---

## -description

Represents an absolute reference to a font face. This interface contains font face type, appropriate file references, and face identification data. It adds new facilities such as comparing two font faces, retrieving font axis values, and retrieving the underlying font resource.

This interface extends [IDWriteFontFace4](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4). Various font data such as metrics, names, and glyph outlines are obtained from **IDWriteFontFace**.

## -see-also

[IDWriteFontFace4](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)
