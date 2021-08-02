---
UID: NF:dwrite.IDWriteFactory.RegisterFontCollectionLoader
title: IDWriteFactory::RegisterFontCollectionLoader (dwrite.h)
description: Registers a custom font collection loader with the factory object.
helpviewer_keywords: ["IDWriteFactory interface [Direct Write]","RegisterFontCollectionLoader method","IDWriteFactory.RegisterFontCollectionLoader","IDWriteFactory::RegisterFontCollectionLoader","RegisterFontCollectionLoader","RegisterFontCollectionLoader method [Direct Write]","RegisterFontCollectionLoader method [Direct Write]","IDWriteFactory interface","directwrite.IDWriteFactory_RegisterFontCollectionLoader","dwrite/IDWriteFactory::RegisterFontCollectionLoader"]
old-location: directwrite\IDWriteFactory_RegisterFontCollectionLoader.htm
tech.root: DirectWrite
ms.assetid: 495f8f56-42b6-4731-a26e-5da2c56a28ed
ms.date: 12/05/2018
ms.keywords: IDWriteFactory interface [Direct Write],RegisterFontCollectionLoader method, IDWriteFactory.RegisterFontCollectionLoader, IDWriteFactory::RegisterFontCollectionLoader, RegisterFontCollectionLoader, RegisterFontCollectionLoader method [Direct Write], RegisterFontCollectionLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_RegisterFontCollectionLoader, dwrite/IDWriteFactory::RegisterFontCollectionLoader
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
 - IDWriteFactory::RegisterFontCollectionLoader
 - dwrite/IDWriteFactory::RegisterFontCollectionLoader
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
 - IDWriteFactory.RegisterFontCollectionLoader
---

# IDWriteFactory::RegisterFontCollectionLoader


## -description

Registers a custom font collection loader with the factory object.

## -parameters

### -param fontCollectionLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a>*</b>

Pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a> object to be registered.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function registers a font collection loader with DirectWrite. The font collection loader interface, which should be implemented by a singleton object, 
      handles enumerating font files in a font collection given a particular type of key. A given instance can only be registered once. Succeeding attempts will return an error, 
      indicating that it has already been registered. Note that font file loader implementations must not register themselves with DirectWrite inside their constructors, 
      and must not unregister themselves inside their destructors, because registration and unregistration operations increment and decrement the object reference count respectively. 
      Instead, registration and unregistration with DirectWrite of font file loaders should be performed outside of the font file loader implementation.

