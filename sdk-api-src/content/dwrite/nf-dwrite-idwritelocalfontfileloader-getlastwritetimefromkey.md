---
UID: NF:dwrite.IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
title: IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey (dwrite.h)
description: Obtains the last write time of the file from the font file reference key.
helpviewer_keywords: ["GetLastWriteTimeFromKey","GetLastWriteTimeFromKey method [Direct Write]","GetLastWriteTimeFromKey method [Direct Write]","IDWriteLocalFontFileLoader interface","IDWriteLocalFontFileLoader interface [Direct Write]","GetLastWriteTimeFromKey method","IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey","IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey","directwrite.idwritelocalfontfileloader_getlastwritetimefromkey","dwrite/IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey"]
old-location: directwrite\idwritelocalfontfileloader_getlastwritetimefromkey.htm
tech.root: DirectWrite
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
ms.date: 12/05/2018
ms.keywords: GetLastWriteTimeFromKey, GetLastWriteTimeFromKey method [Direct Write], GetLastWriteTimeFromKey method [Direct Write],IDWriteLocalFontFileLoader interface, IDWriteLocalFontFileLoader interface [Direct Write],GetLastWriteTimeFromKey method, IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey, IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey, directwrite.idwritelocalfontfileloader_getlastwritetimefromkey, dwrite/IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey
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
 - IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey
 - dwrite/IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey
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
 - IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
---

# IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey


## -description

Obtains the last write time of the file from the font file reference key.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

The font file reference key that uniquely identifies the local font file
    within the scope of the font loader being used.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

The size of font file reference key in bytes.

### -param lastWriteTime [out]

Type: <b>FILETIME*</b>

The time of the last font file modification.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalfontfileloader">IDWriteLocalFontFileLoader</a>

