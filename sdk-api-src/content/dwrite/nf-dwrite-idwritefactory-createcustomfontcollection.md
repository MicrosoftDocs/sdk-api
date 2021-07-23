---
UID: NF:dwrite.IDWriteFactory.CreateCustomFontCollection
title: IDWriteFactory::CreateCustomFontCollection (dwrite.h)
description: Creates a font collection using a custom font collection loader.
helpviewer_keywords: ["CreateCustomFontCollection","CreateCustomFontCollection method [Direct Write]","CreateCustomFontCollection method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateCustomFontCollection method","IDWriteFactory.CreateCustomFontCollection","IDWriteFactory::CreateCustomFontCollection","directwrite.IDWriteFactory_CreateCustomFontCollection","dwrite/IDWriteFactory::CreateCustomFontCollection"]
old-location: directwrite\IDWriteFactory_CreateCustomFontCollection.htm
tech.root: DirectWrite
ms.assetid: 983864bc-b737-4a4d-8f3f-f062eb88cfa7
ms.date: 12/05/2018
ms.keywords: CreateCustomFontCollection, CreateCustomFontCollection method [Direct Write], CreateCustomFontCollection method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateCustomFontCollection method, IDWriteFactory.CreateCustomFontCollection, IDWriteFactory::CreateCustomFontCollection, directwrite.IDWriteFactory_CreateCustomFontCollection, dwrite/IDWriteFactory::CreateCustomFontCollection
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
 - IDWriteFactory::CreateCustomFontCollection
 - dwrite/IDWriteFactory::CreateCustomFontCollection
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
 - IDWriteFactory.CreateCustomFontCollection
---

# IDWriteFactory::CreateCustomFontCollection


## -description

 Creates a font collection using a custom font collection loader.

## -parameters

### -param collectionLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a>*</b>

An application-defined font collection loader, which must have been previously
     registered using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader">RegisterFontCollectionLoader</a>.

### -param collectionKey [in]

Type: <b>const void*</b>

The key used by the loader to identify a collection of font files.  The buffer allocated for this key should at least be the size of <i>collectionKeySize</i>.

### -param collectionKeySize

Type: <b>UINT32</b>

The size, in bytes, of the collection key.

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

Contains  an address of a pointer to the system font collection object if the method succeeds, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

