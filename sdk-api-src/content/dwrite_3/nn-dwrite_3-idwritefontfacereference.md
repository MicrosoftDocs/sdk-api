---
UID: NN:dwrite_3.IDWriteFontFaceReference
title: IDWriteFontFaceReference (dwrite_3.h)
description: Represents a reference to a font face.
helpviewer_keywords: ["IDWriteFontFaceReference","IDWriteFontFaceReference interface [Direct Write]","IDWriteFontFaceReference interface [Direct Write]","described","directwrite.idwritefontfacereference","dwrite_3/IDWriteFontFaceReference"]
old-location: directwrite\idwritefontfacereference.htm
tech.root: DirectWrite
ms.assetid: 04242508-7439-43B6-B3E7-07617B782038
ms.date: 09/10/2025
ms.keywords: IDWriteFontFaceReference, IDWriteFontFaceReference interface [Direct Write], IDWriteFontFaceReference interface [Direct Write],described, directwrite.idwritefontfacereference, dwrite_3/IDWriteFontFaceReference
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteFontFaceReference
 - dwrite_3/IDWriteFontFaceReference
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
 - IDWriteFontFaceReference
---

# IDWriteFontFaceReference interface


## -description

Represents a reference to a font face.
  A uniquely identifying reference to a font, from which you can create a font
  face to query font metrics and use for rendering. A font face reference
  consists of a font file, font face index, and font face simulation. The file
  data may or may not be physically present on the local machine yet.

## -inheritance

The <b>IDWriteFontFaceReference</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFaceReference</b> also has these types of members:

