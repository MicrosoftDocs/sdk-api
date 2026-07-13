---
UID: NN:dwrite_3.IDWriteFontFaceReference1
title: IDWriteFontFaceReference1
description: Represents a reference to a font face. A uniquely identifying reference to a font, from which you can create a font face to query font metrics and use for rendering.
helpviewer_keywords: ["IDWriteFontFaceReference1","IDWriteFontFaceReference1 interface [Direct Write]","IDWriteFontFaceReference1 interface [Direct Write]","described","directwrite.idwritefontfacereference1","dwrite_3/IDWriteFontFaceReference1"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFontFaceReference1, IDWriteFontFaceReference1 interface [Direct Write], IDWriteFontFaceReference1 interface [Direct Write],described, directwrite.idwritefontfacereference1, dwrite_3/IDWriteFontFaceReference1
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
 - IDWriteFontFaceReference1
 - dwrite_3/IDWriteFontFaceReference1
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
 - IDWriteFontFaceReference1
---

## -description

Represents a reference to a font face. A uniquely identifying reference to a font, from which you can create a font face to query font metrics and use for rendering. A font face reference consists of a font file, font face index, and font face simulation. The file data may or may not be physically present on the local machine yet. **IDWriteFontFaceReference1** adds new facilities, including support for [IDWriteFontFace5](./nn-dwrite_3-idwritefontface5.md).

This interface extends [IDWriteFontFaceReference](./nn-dwrite_3-idwritefontfacereference.md).

## -see-also

[IDWriteFontFaceReference](./nn-dwrite_3-idwritefontfacereference.md)
