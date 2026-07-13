---
UID: NF:dwrite.IDWriteFontFile.GetLoader
title: IDWriteFontFile::GetLoader (dwrite.h)
description: Obtains the file loader associated with a font file object.
helpviewer_keywords: ["GetLoader","GetLoader method [Direct Write]","GetLoader method [Direct Write]","IDWriteFontFile interface","IDWriteFontFile interface [Direct Write]","GetLoader method","IDWriteFontFile.GetLoader","IDWriteFontFile::GetLoader","directwrite.IDWriteFontFile_GetLoader","dwrite/IDWriteFontFile::GetLoader"]
old-location: directwrite\IDWriteFontFile_GetLoader.htm
tech.root: DirectWrite
ms.assetid: 60f13a03-2063-4f74-8bfe-217b6c1682ff
ms.date: 12/05/2018
ms.keywords: GetLoader, GetLoader method [Direct Write], GetLoader method [Direct Write],IDWriteFontFile interface, IDWriteFontFile interface [Direct Write],GetLoader method, IDWriteFontFile.GetLoader, IDWriteFontFile::GetLoader, directwrite.IDWriteFontFile_GetLoader, dwrite/IDWriteFontFile::GetLoader
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
 - IDWriteFontFile::GetLoader
 - dwrite/IDWriteFontFile::GetLoader
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
 - IDWriteFontFile.GetLoader
---

# IDWriteFontFile::GetLoader


## -description

 Obtains the file loader associated with a font file object.

## -parameters

### -param fontFileLoader [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>**</b>

When this method returns, contains the address of  a pointer to the font file loader associated with the font file object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>

