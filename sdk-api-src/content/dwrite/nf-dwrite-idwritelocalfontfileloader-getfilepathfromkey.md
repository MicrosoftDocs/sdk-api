---
UID: NF:dwrite.IDWriteLocalFontFileLoader.GetFilePathFromKey
title: IDWriteLocalFontFileLoader::GetFilePathFromKey (dwrite.h)
description: Obtains the absolute font file path from the font file reference key.
helpviewer_keywords: ["GetFilePathFromKey","GetFilePathFromKey method [Direct Write]","GetFilePathFromKey method [Direct Write]","IDWriteLocalFontFileLoader interface","IDWriteLocalFontFileLoader interface [Direct Write]","GetFilePathFromKey method","IDWriteLocalFontFileLoader.GetFilePathFromKey","IDWriteLocalFontFileLoader::GetFilePathFromKey","directwrite.idwritelocalfontfileloader_getfilepathfromkey","dwrite/IDWriteLocalFontFileLoader::GetFilePathFromKey"]
old-location: directwrite\idwritelocalfontfileloader_getfilepathfromkey.htm
tech.root: DirectWrite
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
ms.date: 12/05/2018
ms.keywords: GetFilePathFromKey, GetFilePathFromKey method [Direct Write], GetFilePathFromKey method [Direct Write],IDWriteLocalFontFileLoader interface, IDWriteLocalFontFileLoader interface [Direct Write],GetFilePathFromKey method, IDWriteLocalFontFileLoader.GetFilePathFromKey, IDWriteLocalFontFileLoader::GetFilePathFromKey, directwrite.idwritelocalfontfileloader_getfilepathfromkey, dwrite/IDWriteLocalFontFileLoader::GetFilePathFromKey
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteLocalFontFileLoader::GetFilePathFromKey
 - dwrite/IDWriteLocalFontFileLoader::GetFilePathFromKey
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
 - IDWriteLocalFontFileLoader.GetFilePathFromKey
---

# IDWriteLocalFontFileLoader::GetFilePathFromKey


## -description

Obtains the absolute font file path from the font file reference key.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

The font file reference key that uniquely identifies the local font file
    within the scope of the font loader being used.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

The size of font file reference key in bytes.

### -param filePath [out]

Type: <b>WCHAR*</b>

The character array that receives the local file path.

### -param filePathSize

Type: <b>UINT32</b>

The length of the file path character array.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalfontfileloader">IDWriteLocalFontFileLoader</a>

