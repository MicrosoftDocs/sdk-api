---
UID: NN:dwrite_2.IDWriteFontFace2
title: IDWriteFontFace2
description: Contains font face type, appropriate file references, and face identification data.
helpviewer_keywords: ["IDWriteFontFace2","IDWriteFontFace2 interface [Direct Write]","IDWriteFontFace2 interface [Direct Write]","described","IDWriteFontFace2","directwrite.idwritefontface2","dwrite_2/IDWriteFontFace2"]
old-location: directwrite\idwritefontface2.htm
tech.root: DirectWrite
ms.assetid: D74F6472-CEEC-4DF5-83C8-0D65923C8028
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace2, IDWriteFontFace2 interface [Direct Write], IDWriteFontFace2 interface [Direct Write],described, IDWriteFontFace2, directwrite.idwritefontface2, dwrite_2/IDWriteFontFace2
f1_keywords:
- dwrite_2/IDWriteFontFace2
dev_langs:
- c++
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFontFace2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Represents an absolute reference to a font face. This interface contains font face type, appropriate file references, and face identification data. It adds the ability to check whether a color rendering path is potentially necessary.

This interface extends [IDWriteFontFace1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1). Various font data such as metrics, names, and glyph outlines are obtained from **IDWriteFontFace**.

## -see-also

[IDWriteFontFace1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)
