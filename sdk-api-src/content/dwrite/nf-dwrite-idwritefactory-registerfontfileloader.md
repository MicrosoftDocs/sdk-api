---
UID: NF:dwrite.IDWriteFactory.RegisterFontFileLoader
title: IDWriteFactory::RegisterFontFileLoader (dwrite.h)
description: Registers a font file loader with DirectWrite.
helpviewer_keywords: ["IDWriteFactory interface [Direct Write]","RegisterFontFileLoader method","IDWriteFactory.RegisterFontFileLoader","IDWriteFactory::RegisterFontFileLoader","RegisterFontFileLoader","RegisterFontFileLoader method [Direct Write]","RegisterFontFileLoader method [Direct Write]","IDWriteFactory interface","directwrite.IDWriteFactory_RegisterFontFileLoader","dwrite/IDWriteFactory::RegisterFontFileLoader"]
old-location: directwrite\IDWriteFactory_RegisterFontFileLoader.htm
tech.root: DirectWrite
ms.assetid: f5b28c3d-c3ad-4435-92c8-07841e8d160a
ms.date: 12/05/2018
ms.keywords: IDWriteFactory interface [Direct Write],RegisterFontFileLoader method, IDWriteFactory.RegisterFontFileLoader, IDWriteFactory::RegisterFontFileLoader, RegisterFontFileLoader, RegisterFontFileLoader method [Direct Write], RegisterFontFileLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_RegisterFontFileLoader, dwrite/IDWriteFactory::RegisterFontFileLoader
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
 - IDWriteFactory::RegisterFontFileLoader
 - dwrite/IDWriteFactory::RegisterFontFileLoader
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
 - IDWriteFactory.RegisterFontFileLoader
---

# IDWriteFactory::RegisterFontFileLoader


## -description

 Registers a font file loader with DirectWrite.

## -parameters

### -param fontFileLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>*</b>

Pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a> object for a particular file resource type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This function registers a font file loader with DirectWrite.
     The font file loader interface, which should be implemented   by a singleton object, handles loading font file resources of a particular type from a key.
     A given instance can only be registered once.
     Succeeding attempts will return an error, indicating that it has already been registered.
     Note that font file loader implementations must not register themselves with DirectWrite
     inside their constructors, and must not unregister themselves inside their destructors, because
     registration and unregistration operations increment and decrement the object reference count respectively.
     Instead, registration and unregistration with DirectWrite of font file loaders should be performed
     outside of the font file loader implementation.

