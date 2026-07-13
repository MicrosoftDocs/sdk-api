---
UID: NF:dwrite.IDWriteFontFamily.GetMatchingFonts
title: IDWriteFontFamily::GetMatchingFonts (dwrite.h)
description: Gets a list of fonts in the font family ranked in order of how well they match the specified properties.
helpviewer_keywords: ["GetMatchingFonts","GetMatchingFonts method [Direct Write]","GetMatchingFonts method [Direct Write]","IDWriteFontFamily interface","IDWriteFontFamily interface [Direct Write]","GetMatchingFonts method","IDWriteFontFamily.GetMatchingFonts","IDWriteFontFamily::GetMatchingFonts","directwrite.IDWriteFontFamily_GetMatchingFonts","dwrite/IDWriteFontFamily::GetMatchingFonts"]
old-location: directwrite\IDWriteFontFamily_GetMatchingFonts.htm
tech.root: DirectWrite
ms.assetid: 81984e35-7b62-4e14-9ded-45cee49a8921
ms.date: 12/05/2018
ms.keywords: GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontFamily interface, IDWriteFontFamily interface [Direct Write],GetMatchingFonts method, IDWriteFontFamily.GetMatchingFonts, IDWriteFontFamily::GetMatchingFonts, directwrite.IDWriteFontFamily_GetMatchingFonts, dwrite/IDWriteFontFamily::GetMatchingFonts
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
 - IDWriteFontFamily::GetMatchingFonts
 - dwrite/IDWriteFontFamily::GetMatchingFonts
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
 - IDWriteFontFamily.GetMatchingFonts
---

# IDWriteFontFamily::GetMatchingFonts


## -description

 Gets a list of fonts in the font family ranked in order of how well they match the specified properties.

## -parameters

### -param weight

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a></b>

A value that is used to match a requested font weight.

### -param stretch

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch">DWRITE_FONT_STRETCH</a></b>

A value that is used to match a requested font stretch.

### -param style

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a></b>

A value that is used to match a requested font style.

### -param matchingFonts [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a>**</b>

An address of a pointer to the newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily">IDWriteFontFamily</a>

