---
UID: NF:dwrite_3.IDWriteFontSet.FindFontFace
title: IDWriteFontSet::FindFontFace (dwrite_3.h)
description: Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.
helpviewer_keywords: ["FindFontFace","FindFontFace method [Direct Write]","FindFontFace method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","FindFontFace method","IDWriteFontSet.FindFontFace","IDWriteFontSet::FindFontFace","directwrite.idwritefontset_findfontface","dwrite_3/IDWriteFontSet::FindFontFace"]
old-location: directwrite\idwritefontset_findfontface.htm
tech.root: DirectWrite
ms.assetid: dcb8ddbd-9c82-cd90-f4bd-490855d93efd
ms.date: 12/05/2018
ms.keywords: FindFontFace, FindFontFace method [Direct Write], FindFontFace method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],FindFontFace method, IDWriteFontSet.FindFontFace, IDWriteFontSet::FindFontFace, directwrite.idwritefontset_findfontface, dwrite_3/IDWriteFontSet::FindFontFace
f1_keywords:
- dwrite_3/IDWriteFontSet.FindFontFace
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFontSet.FindFontFace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontSet::FindFontFace


## -description


Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.


## -parameters




### -param fontFace

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

Font face object that specifies the physical font.


### -param listIndex [out]

Type: <b>UINT32*</b>

Receives the zero-based index of the matching font if the font was found, or UINT_MAX otherwise.


### -param exists [out]

Type: <b>BOOL*</b>

Receives TRUE if the font exists or FALSE otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>
 

 

