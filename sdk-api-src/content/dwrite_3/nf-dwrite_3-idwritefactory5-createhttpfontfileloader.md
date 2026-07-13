---
UID: NF:dwrite_3.IDWriteFactory5.CreateHttpFontFileLoader
title: IDWriteFactory5::CreateHttpFontFileLoader (dwrite_3.h)
description: Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.
helpviewer_keywords: ["CreateHttpFontFileLoader","CreateHttpFontFileLoader method [Direct Write]","CreateHttpFontFileLoader method [Direct Write]","IDWriteFactory5 interface","IDWriteFactory5 interface [Direct Write]","CreateHttpFontFileLoader method","IDWriteFactory5.CreateHttpFontFileLoader","IDWriteFactory5::CreateHttpFontFileLoader","directwrite.idwritefactory5_createhttpfontfileloader","dwrite_3/IDWriteFactory5::CreateHttpFontFileLoader"]
old-location: directwrite\idwritefactory5_createhttpfontfileloader.htm
tech.root: DirectWrite
ms.assetid: 7C8D581E-489D-48BE-8B3F-278E1C246BBA
ms.date: 09/10/2025
ms.keywords: CreateHttpFontFileLoader, CreateHttpFontFileLoader method [Direct Write], CreateHttpFontFileLoader method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],CreateHttpFontFileLoader method, IDWriteFactory5.CreateHttpFontFileLoader, IDWriteFactory5::CreateHttpFontFileLoader, directwrite.idwritefactory5_createhttpfontfileloader, dwrite_3/IDWriteFactory5::CreateHttpFontFileLoader
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
 - IDWriteFactory5::CreateHttpFontFileLoader
 - dwrite_3/IDWriteFactory5::CreateHttpFontFileLoader
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
 - IDWriteFactory5.CreateHttpFontFileLoader
---

# IDWriteFactory5::CreateHttpFontFileLoader


## -description

Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.

## -parameters

### -param referrerUrl

Type: <b>wchar_t const*</b>

Optional referrer URL for HTTP requests.

### -param extraHeaders

Type: <b>wchar_t const*</b>

Optional additional header fields to include in HTTP requests. Each header field consists of a name followed by a colon (":") and the field value, as specified by RFC 2616. Multiple header fields may be separated by newlines.

### -param newLoader [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>**</b>

Receives a pointer to the newly-created loader object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an **HRESULT** success or error code.

## -see-also

[Creating a custom font set using known, remote fonts on the Web](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a>

