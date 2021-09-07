---
UID: NF:dwrite.IDWriteFontFile.GetReferenceKey
title: IDWriteFontFile::GetReferenceKey (dwrite.h)
description: Obtains the pointer to the reference key of a font file. The returned pointer is valid until the font file object is released.
helpviewer_keywords: ["GetReferenceKey","GetReferenceKey method [Direct Write]","GetReferenceKey method [Direct Write]","IDWriteFontFile interface","IDWriteFontFile interface [Direct Write]","GetReferenceKey method","IDWriteFontFile.GetReferenceKey","IDWriteFontFile::GetReferenceKey","directwrite.IDWriteFontFile_GetReferenceKey","dwrite/IDWriteFontFile::GetReferenceKey"]
old-location: directwrite\IDWriteFontFile_GetReferenceKey.htm
tech.root: DirectWrite
ms.assetid: 2f76f0a0-2b4a-4983-88b9-0f1f2b7a7027
ms.date: 12/05/2018
ms.keywords: GetReferenceKey, GetReferenceKey method [Direct Write], GetReferenceKey method [Direct Write],IDWriteFontFile interface, IDWriteFontFile interface [Direct Write],GetReferenceKey method, IDWriteFontFile.GetReferenceKey, IDWriteFontFile::GetReferenceKey, directwrite.IDWriteFontFile_GetReferenceKey, dwrite/IDWriteFontFile::GetReferenceKey
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFontFile::GetReferenceKey
 - dwrite/IDWriteFontFile::GetReferenceKey
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
 - IDWriteFontFile.GetReferenceKey
---

# IDWriteFontFile::GetReferenceKey


## -description

 Obtains the pointer to the reference key of a font file. The returned pointer is valid until the font file object is released.

## -parameters

### -param fontFileReferenceKey [out]

Type: <b>const void**</b>

When this method returns, contains an address of  a pointer to the font file reference key. Note that the pointer value is only valid until the font file object it is obtained from is released. This parameter is passed uninitialized.

### -param fontFileReferenceKeySize [out]

Type: <b>UINT32*</b>

When this method returns, contains the size of the font file reference key in bytes. This parameter is passed uninitialized.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>

