---
UID: NN:dwrite_3.IDWriteFontFace5
title: IDWriteFontFace5
description: Contains font face type, appropriate file references, and face identification data. (IDWriteFontFace5)
helpviewer_keywords: ["IDWriteFontFace5","IDWriteFontFace5 interface [Direct Write]","IDWriteFontFace5 interface [Direct Write]","described","directwrite.idwritefontface5","dwrite_3/IDWriteFontFace5"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5, IDWriteFontFace5 interface [Direct Write], IDWriteFontFace5 interface [Direct Write],described, directwrite.idwritefontface5, dwrite_3/IDWriteFontFace5
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
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
req.target-type: Windows
req.unicode-ansi: 
f1_keywords:
 - IDWriteFontFace5
 - dwrite_3/IDWriteFontFace5
dev_langs:
 - c++
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

This interface extends [IDWriteFontFace4](./nn-dwrite_3-idwritefontface4.md). Various font data such as metrics, names, and glyph outlines are obtained from **IDWriteFontFace**.

## -see-also

[IDWriteFontFace4](./nn-dwrite_3-idwritefontface4.md)
