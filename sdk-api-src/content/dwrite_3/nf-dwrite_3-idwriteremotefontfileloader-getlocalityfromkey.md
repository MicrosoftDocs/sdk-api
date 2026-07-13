---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.GetLocalityFromKey
title: IDWriteRemoteFontFileLoader::GetLocalityFromKey (dwrite_3.h)
description: Gets the locality of the file resource identified by the unique key.
helpviewer_keywords: ["GetLocalityFromKey","GetLocalityFromKey method [Direct Write]","GetLocalityFromKey method [Direct Write]","IDWriteRemoteFontFileLoader interface","IDWriteRemoteFontFileLoader interface [Direct Write]","GetLocalityFromKey method","IDWriteRemoteFontFileLoader.GetLocalityFromKey","IDWriteRemoteFontFileLoader::GetLocalityFromKey","directwrite.idwriteremotefontfileloader_getlocalityfromkey","dwrite_3/IDWriteRemoteFontFileLoader::GetLocalityFromKey"]
old-location: directwrite\idwriteremotefontfileloader_getlocalityfromkey.htm
tech.root: DirectWrite
ms.assetid: 997D8F04-8667-4D90-B097-CD48F979BE02
ms.date: 09/10/2025
ms.keywords: GetLocalityFromKey, GetLocalityFromKey method [Direct Write], GetLocalityFromKey method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],GetLocalityFromKey method, IDWriteRemoteFontFileLoader.GetLocalityFromKey, IDWriteRemoteFontFileLoader::GetLocalityFromKey, directwrite.idwriteremotefontfileloader_getlocalityfromkey, dwrite_3/IDWriteRemoteFontFileLoader::GetLocalityFromKey
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
 - IDWriteRemoteFontFileLoader::GetLocalityFromKey
 - dwrite_3/IDWriteRemoteFontFileLoader::GetLocalityFromKey
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
 - IDWriteRemoteFontFileLoader.GetLocalityFromKey
---

# IDWriteRemoteFontFileLoader::GetLocalityFromKey


## -description

Gets the locality of the file resource identified by the unique key.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>void</b>

Font file reference key that uniquely identifies the font file resource within the scope of the font loader being used.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

Size of font file reference key in bytes.

### -param locality [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality">DWRITE_LOCALITY</a>*</b>

Locality of the file.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>

