---
UID: NF:dwrite.IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
title: IDWriteLocalFontFileLoader::GetFilePathLengthFromKey (dwrite.h)
description: Obtains the length of the absolute file path from the font file reference key.
helpviewer_keywords: ["GetFilePathLengthFromKey","GetFilePathLengthFromKey method [Direct Write]","GetFilePathLengthFromKey method [Direct Write]","IDWriteLocalFontFileLoader interface","IDWriteLocalFontFileLoader interface [Direct Write]","GetFilePathLengthFromKey method","IDWriteLocalFontFileLoader.GetFilePathLengthFromKey","IDWriteLocalFontFileLoader::GetFilePathLengthFromKey","directwrite.idwritelocalfontfileloader_getfilepathlengthfromkey","dwrite/IDWriteLocalFontFileLoader::GetFilePathLengthFromKey"]
old-location: directwrite\idwritelocalfontfileloader_getfilepathlengthfromkey.htm
tech.root: DirectWrite
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
ms.date: 12/05/2018
ms.keywords: GetFilePathLengthFromKey, GetFilePathLengthFromKey method [Direct Write], GetFilePathLengthFromKey method [Direct Write],IDWriteLocalFontFileLoader interface, IDWriteLocalFontFileLoader interface [Direct Write],GetFilePathLengthFromKey method, IDWriteLocalFontFileLoader.GetFilePathLengthFromKey, IDWriteLocalFontFileLoader::GetFilePathLengthFromKey, directwrite.idwritelocalfontfileloader_getfilepathlengthfromkey, dwrite/IDWriteLocalFontFileLoader::GetFilePathLengthFromKey
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
 - IDWriteLocalFontFileLoader::GetFilePathLengthFromKey
 - dwrite/IDWriteLocalFontFileLoader::GetFilePathLengthFromKey
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
 - IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
---

# IDWriteLocalFontFileLoader::GetFilePathLengthFromKey


## -description

Obtains the length of the absolute file path from the font file reference key.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

Font file reference key that uniquely identifies the local font file
    within the scope of the font loader being used.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

Size of font file reference key in bytes.

### -param filePathLength [out]

Type: <b>UINT32*</b>

Length of the file path string, not including the terminated <b>NULL</b> character.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalfontfileloader">IDWriteLocalFontFileLoader</a>

