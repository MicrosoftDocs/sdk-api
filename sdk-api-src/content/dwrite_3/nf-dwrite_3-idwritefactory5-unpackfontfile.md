---
UID: NF:dwrite_3.IDWriteFactory5.UnpackFontFile
title: IDWriteFactory5::UnpackFontFile (dwrite_3.h)
description: The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.
helpviewer_keywords: ["IDWriteFactory5 interface [Direct Write]","UnpackFontFile method","IDWriteFactory5.UnpackFontFile","IDWriteFactory5::UnpackFontFile","UnpackFontFile","UnpackFontFile method [Direct Write]","UnpackFontFile method [Direct Write]","IDWriteFactory5 interface","directwrite.idwritefactory5_unpackfontfile","dwrite_3/IDWriteFactory5::UnpackFontFile"]
old-location: directwrite\idwritefactory5_unpackfontfile.htm
tech.root: DirectWrite
ms.assetid: F82863DC-BFC8-49D3-93C5-DCA45093F81A
ms.date: 09/10/2025
ms.keywords: IDWriteFactory5 interface [Direct Write],UnpackFontFile method, IDWriteFactory5.UnpackFontFile, IDWriteFactory5::UnpackFontFile, UnpackFontFile, UnpackFontFile method [Direct Write], UnpackFontFile method [Direct Write],IDWriteFactory5 interface, directwrite.idwritefactory5_unpackfontfile, dwrite_3/IDWriteFactory5::UnpackFontFile
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
 - IDWriteFactory5::UnpackFontFile
 - dwrite_3/IDWriteFactory5::UnpackFontFile
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
 - IDWriteFactory5.UnpackFontFile
---

# IDWriteFactory5::UnpackFontFile


## -description

The UnpackFontFile method unpacks font data from a container file (WOFF or WOFF2) and returns the unpacked font data in the form of a font file stream.

## -parameters

### -param containerType

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type">DWRITE_CONTAINER_TYPE</a></b>

Container type returned by AnalyzeContainerType.

### -param fileData [in]

Type: <b>void</b>

Pointer to the compressed data.

### -param fileDataSize

Type: <b>UINT32</b>

Size of the compressed data, in bytes.

### -param unpackedFontStream [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>**</b>

Receives a pointer to a newly created font file stream containing the uncompressed data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Standard HRESULT error code. The return value is E_INVALIDARG if the container type is DWRITE_CONTAINER_TYPE_UNKNOWN.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a>

