---
UID: NF:dwrite.IDWriteFactory.UnregisterFontFileLoader
title: IDWriteFactory::UnregisterFontFileLoader (dwrite.h)
description: Unregisters a font file loader that was previously registered with the DirectWrite font system using RegisterFontFileLoader.
helpviewer_keywords: ["IDWriteFactory interface [Direct Write]","UnregisterFontFileLoader method","IDWriteFactory.UnregisterFontFileLoader","IDWriteFactory::UnregisterFontFileLoader","UnregisterFontFileLoader","UnregisterFontFileLoader method [Direct Write]","UnregisterFontFileLoader method [Direct Write]","IDWriteFactory interface","directwrite.IDWriteFactory_UnregisterFontFileLoader","dwrite/IDWriteFactory::UnregisterFontFileLoader"]
old-location: directwrite\IDWriteFactory_UnregisterFontFileLoader.htm
tech.root: DirectWrite
ms.assetid: f048671e-dfb6-449d-9bcd-e5df8408c01a
ms.date: 12/05/2018
ms.keywords: IDWriteFactory interface [Direct Write],UnregisterFontFileLoader method, IDWriteFactory.UnregisterFontFileLoader, IDWriteFactory::UnregisterFontFileLoader, UnregisterFontFileLoader, UnregisterFontFileLoader method [Direct Write], UnregisterFontFileLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_UnregisterFontFileLoader, dwrite/IDWriteFactory::UnregisterFontFileLoader
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
 - IDWriteFactory::UnregisterFontFileLoader
 - dwrite/IDWriteFactory::UnregisterFontFileLoader
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
 - IDWriteFactory.UnregisterFontFileLoader
---

# IDWriteFactory::UnregisterFontFileLoader


## -description

 Unregisters a font file loader that was previously registered with the DirectWrite font system using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">RegisterFontFileLoader</a>.

## -parameters

### -param fontFileLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>*</b>

Pointer to the file loader that was previously registered with the DirectWrite font system using <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">RegisterFontFileLoader</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This function unregisters font file loader callbacks with the DirectWrite font system.
     You should implement the font file loader interface by a singleton object.
     Note that font file loader implementations must not register themselves with DirectWrite
     inside their constructors and must not unregister themselves in their destructors, because
     registration and unregistration operations increment and decrement the object reference count respectively.
     Instead, registration and unregistration of font file loaders with DirectWrite should be performed
     outside of the font file loader implementation.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

