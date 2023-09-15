---
UID: NF:dwrite_2.IDWriteFactory2.CreateFontFallbackBuilder
title: IDWriteFactory2::CreateFontFallbackBuilder (dwrite_2.h)
description: Creates a font fallback builder object.
helpviewer_keywords: ["CreateFontFallbackBuilder","CreateFontFallbackBuilder method [Direct Write]","CreateFontFallbackBuilder method [Direct Write]","IDWriteFactory2 interface","IDWriteFactory2 interface [Direct Write]","CreateFontFallbackBuilder method","IDWriteFactory2.CreateFontFallbackBuilder","IDWriteFactory2::CreateFontFallbackBuilder","directwrite.idwritefactory2_createfontfallbackbuilder","dwrite_2/IDWriteFactory2::CreateFontFallbackBuilder"]
old-location: directwrite\idwritefactory2_createfontfallbackbuilder.htm
tech.root: DirectWrite
ms.assetid: 98A6DE80-0084-4D28-B456-8E572D565915
ms.date: 12/05/2018
ms.keywords: CreateFontFallbackBuilder, CreateFontFallbackBuilder method [Direct Write], CreateFontFallbackBuilder method [Direct Write],IDWriteFactory2 interface, IDWriteFactory2 interface [Direct Write],CreateFontFallbackBuilder method, IDWriteFactory2.CreateFontFallbackBuilder, IDWriteFactory2::CreateFontFallbackBuilder, directwrite.idwritefactory2_createfontfallbackbuilder, dwrite_2/IDWriteFactory2::CreateFontFallbackBuilder
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory2::CreateFontFallbackBuilder
 - dwrite_2/IDWriteFactory2::CreateFontFallbackBuilder
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
 - IDWriteFactory2.CreateFontFallbackBuilder
---

# IDWriteFactory2::CreateFontFallbackBuilder


## -description

Creates a font fallback builder object.

A font fall back builder allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.

## -parameters

### -param fontFallbackBuilder [out]

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallbackbuilder">IDWriteFontFallbackBuilder</a>**</b>

Contains an address of a pointer to the newly created font fallback builder object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefactory2">IDWriteFactory2</a>

