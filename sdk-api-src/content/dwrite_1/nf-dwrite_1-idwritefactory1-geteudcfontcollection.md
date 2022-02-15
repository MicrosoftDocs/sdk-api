---
UID: NF:dwrite_1.IDWriteFactory1.GetEudcFontCollection
title: IDWriteFactory1::GetEudcFontCollection (dwrite_1.h)
description: Gets a font collection representing the set of EUDC (end-user defined characters) fonts.
helpviewer_keywords: ["GetEudcFontCollection","GetEudcFontCollection method [Direct Write]","GetEudcFontCollection method [Direct Write]","IDWriteFactory1 interface","IDWriteFactory1 interface [Direct Write]","GetEudcFontCollection method","IDWriteFactory1.GetEudcFontCollection","IDWriteFactory1::GetEudcFontCollection","directwrite.idwritefactory1_geteudcfontcollection","dwrite_1/IDWriteFactory1::GetEudcFontCollection"]
old-location: directwrite\idwritefactory1_geteudcfontcollection.htm
tech.root: DirectWrite
ms.assetid: 7A0B476D-6158-4AE1-B66F-8168E4AE7DE4
ms.date: 12/05/2018
ms.keywords: GetEudcFontCollection, GetEudcFontCollection method [Direct Write], GetEudcFontCollection method [Direct Write],IDWriteFactory1 interface, IDWriteFactory1 interface [Direct Write],GetEudcFontCollection method, IDWriteFactory1.GetEudcFontCollection, IDWriteFactory1::GetEudcFontCollection, directwrite.idwritefactory1_geteudcfontcollection, dwrite_1/IDWriteFactory1::GetEudcFontCollection
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteFactory1::GetEudcFontCollection
 - dwrite_1/IDWriteFactory1::GetEudcFontCollection
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
 - IDWriteFactory1.GetEudcFontCollection
---

# IDWriteFactory1::GetEudcFontCollection


## -description

Gets a font collection representing the set of EUDC (end-user defined characters) fonts.

## -parameters

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

The font collection to fill.

### -param checkForUpdates

Type: <b>BOOL</b>

Whether to check for updates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note that if no EUDC is set on the system,
    the returned collection will be empty, meaning it will return success
    but GetFontFamilyCount will be zero.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1">IDWriteFactory1</a>

