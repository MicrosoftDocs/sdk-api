---
UID: NF:dwrite.IDWriteFactory.UnregisterFontCollectionLoader
title: IDWriteFactory::UnregisterFontCollectionLoader (dwrite.h)
description: Unregisters a custom font collection loader that was previously registered using RegisterFontCollectionLoader.
helpviewer_keywords: ["IDWriteFactory interface [Direct Write]","UnregisterFontCollectionLoader method","IDWriteFactory.UnregisterFontCollectionLoader","IDWriteFactory::UnregisterFontCollectionLoader","UnregisterFontCollectionLoader","UnregisterFontCollectionLoader method [Direct Write]","UnregisterFontCollectionLoader method [Direct Write]","IDWriteFactory interface","directwrite.IDWriteFactory_UnregisterFontCollectionLoader","dwrite/IDWriteFactory::UnregisterFontCollectionLoader"]
old-location: directwrite\IDWriteFactory_UnregisterFontCollectionLoader.htm
tech.root: DirectWrite
ms.assetid: 6a8682e3-72de-4afd-b9db-ba9b0d79f195
ms.date: 12/05/2018
ms.keywords: IDWriteFactory interface [Direct Write],UnregisterFontCollectionLoader method, IDWriteFactory.UnregisterFontCollectionLoader, IDWriteFactory::UnregisterFontCollectionLoader, UnregisterFontCollectionLoader, UnregisterFontCollectionLoader method [Direct Write], UnregisterFontCollectionLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_UnregisterFontCollectionLoader, dwrite/IDWriteFactory::UnregisterFontCollectionLoader
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
 - IDWriteFactory::UnregisterFontCollectionLoader
 - dwrite/IDWriteFactory::UnregisterFontCollectionLoader
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
 - IDWriteFactory.UnregisterFontCollectionLoader
---

# IDWriteFactory::UnregisterFontCollectionLoader


## -description

 Unregisters a custom font collection loader that was previously registered using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader">RegisterFontCollectionLoader</a>.

## -parameters

### -param fontCollectionLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a>*</b>

Pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a> object to be unregistered.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

