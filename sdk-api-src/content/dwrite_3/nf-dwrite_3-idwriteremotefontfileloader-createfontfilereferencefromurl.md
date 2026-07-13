---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl
title: IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl (dwrite_3.h)
description: Creates a font file reference from a URL if the loader supports this capability.
helpviewer_keywords: ["CreateFontFileReferenceFromUrl","CreateFontFileReferenceFromUrl method [Direct Write]","CreateFontFileReferenceFromUrl method [Direct Write]","IDWriteRemoteFontFileLoader interface","IDWriteRemoteFontFileLoader interface [Direct Write]","CreateFontFileReferenceFromUrl method","IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl","IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl","directwrite.idwriteremotefontfileloader_createfontfilereferencefromurl","dwrite_3/IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl"]
old-location: directwrite\idwriteremotefontfileloader_createfontfilereferencefromurl.htm
tech.root: DirectWrite
ms.assetid: C8695514-532F-4CAC-9A50-049C81812F15
ms.date: 09/10/2025
ms.keywords: CreateFontFileReferenceFromUrl, CreateFontFileReferenceFromUrl method [Direct Write], CreateFontFileReferenceFromUrl method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],CreateFontFileReferenceFromUrl method, IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl, IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl, directwrite.idwriteremotefontfileloader_createfontfilereferencefromurl, dwrite_3/IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl
 - dwrite_3/IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl
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
 - IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl
---

# IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl


## -description

Creates a font file reference from a URL if the loader supports this capability.

## -parameters

### -param factory

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>*</b>

Factory used to create the font file reference.

### -param baseUrl

Type: <b>WCHAR</b>

Optional base URL. The base URL is used to resolve the fontFileUrl if it is relative. For example, the baseUrl might be the URL of the referring document
          that contained the fontFileUrl.

### -param fontFileUrl [in]

Type: <b>WCHAR</b>

URL of the font resource.

### -param fontFile [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

Receives a pointer to the newly created font file reference.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

If baseUrl is a non-empty string, then baseUrl concatenated with fontFileUrl should form a valid URL, DirectWrite will not supply any additional delimiter.

## -see-also

[Creating a custom font set using known, remote fonts on the Web](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>

