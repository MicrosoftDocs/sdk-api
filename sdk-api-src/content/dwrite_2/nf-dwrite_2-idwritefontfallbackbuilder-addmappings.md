---
UID: NF:dwrite_2.IDWriteFontFallbackBuilder.AddMappings
title: IDWriteFontFallbackBuilder::AddMappings (dwrite_2.h)
description: Add all the mappings from an existing font fallback object.
helpviewer_keywords: ["AddMappings","AddMappings method [Direct Write]","AddMappings method [Direct Write]","IDWriteFontFallbackBuilder interface","IDWriteFontFallbackBuilder interface [Direct Write]","AddMappings method","IDWriteFontFallbackBuilder.AddMappings","IDWriteFontFallbackBuilder::AddMappings","directwrite.idwritefontfallbackbuilder_addmappings","dwrite_2/IDWriteFontFallbackBuilder::AddMappings"]
old-location: directwrite\idwritefontfallbackbuilder_addmappings.htm
tech.root: DirectWrite
ms.assetid: 8CC8BFD3-4177-4CA0-A74C-43CCDEAA7D74
ms.date: 12/05/2018
ms.keywords: AddMappings, AddMappings method [Direct Write], AddMappings method [Direct Write],IDWriteFontFallbackBuilder interface, IDWriteFontFallbackBuilder interface [Direct Write],AddMappings method, IDWriteFontFallbackBuilder.AddMappings, IDWriteFontFallbackBuilder::AddMappings, directwrite.idwritefontfallbackbuilder_addmappings, dwrite_2/IDWriteFontFallbackBuilder::AddMappings
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
 - IDWriteFontFallbackBuilder::AddMappings
 - dwrite_2/IDWriteFontFallbackBuilder::AddMappings
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
 - IDWriteFontFallbackBuilder.AddMappings
---

## -description

Adds all the mappings from an existing font fallback object, which can be used to compose larger fallback definitions. A common scenario is to start with the system fallback from [IDWriteFactory2::GetSystemFontFallback](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-getsystemfontfallback) to cover the majority of Unicode characters, but then customize a few ranges with additional application-specific entries, either appending them first (to have priority over the system default) before calling **AddMappings**; or calling **AddMappings** first, and then appending custom ranges to fill in any custom gaps.

## -parameters

### -param fontFallback

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback">IDWriteFontFallback</a>*</b>

An existing font fallback object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallbackbuilder">IDWriteFontFallbackBuilder</a>

