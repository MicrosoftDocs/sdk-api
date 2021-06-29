---
UID: NF:dwrite.IDWriteFontFace.GetIndex
title: IDWriteFontFace::GetIndex (dwrite.h)
description: Obtains the index of a font face in the context of its font files.
helpviewer_keywords: ["GetIndex","GetIndex method [Direct Write]","GetIndex method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetIndex method","IDWriteFontFace.GetIndex","IDWriteFontFace::GetIndex","directwrite.IDWriteFontFace_GetIndex","dwrite/IDWriteFontFace::GetIndex"]
old-location: directwrite\IDWriteFontFace_GetIndex.htm
tech.root: DirectWrite
ms.assetid: 69c87fcf-775c-4c6d-971c-e1bb999d246b
ms.date: 12/05/2018
ms.keywords: GetIndex, GetIndex method [Direct Write], GetIndex method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetIndex method, IDWriteFontFace.GetIndex, IDWriteFontFace::GetIndex, directwrite.IDWriteFontFace_GetIndex, dwrite/IDWriteFontFace::GetIndex
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFontFace::GetIndex
 - dwrite/IDWriteFontFace::GetIndex
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
 - IDWriteFontFace.GetIndex
---

# IDWriteFontFace::GetIndex


## -description

 Obtains the index of a font face in the context of its font files.



## -returns

Type: <b>UINT32</b>

The zero-based index of a font face in cases when the font files contain a collection of font faces.
     If the font files contain a single face, this value is zero.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

