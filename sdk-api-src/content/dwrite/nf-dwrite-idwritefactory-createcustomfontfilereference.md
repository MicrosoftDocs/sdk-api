---
UID: NF:dwrite.IDWriteFactory.CreateCustomFontFileReference
title: IDWriteFactory::CreateCustomFontFileReference (dwrite.h)
description: Creates a reference to an application-specific font file resource.
helpviewer_keywords: ["CreateCustomFontFileReference","CreateCustomFontFileReference method [Direct Write]","CreateCustomFontFileReference method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateCustomFontFileReference method","IDWriteFactory.CreateCustomFontFileReference","IDWriteFactory::CreateCustomFontFileReference","directwrite.IDWriteFactory_CreateCustomFontFileReference","dwrite/IDWriteFactory::CreateCustomFontFileReference"]
old-location: directwrite\IDWriteFactory_CreateCustomFontFileReference.htm
tech.root: DirectWrite
ms.assetid: 1c82ffcd-3e43-47cd-9a6c-ff8bd1d2625f
ms.date: 12/05/2018
ms.keywords: CreateCustomFontFileReference, CreateCustomFontFileReference method [Direct Write], CreateCustomFontFileReference method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateCustomFontFileReference method, IDWriteFactory.CreateCustomFontFileReference, IDWriteFactory::CreateCustomFontFileReference, directwrite.IDWriteFactory_CreateCustomFontFileReference, dwrite/IDWriteFactory::CreateCustomFontFileReference
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
 - IDWriteFactory::CreateCustomFontFileReference
 - dwrite/IDWriteFactory::CreateCustomFontFileReference
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
 - IDWriteFactory.CreateCustomFontFileReference
---

# IDWriteFactory::CreateCustomFontFileReference


## -description

 Creates a reference to an application-specific font file resource.

## -parameters

### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

A font file reference key that uniquely identifies the font file resource
     during the lifetime of <i>fontFileLoader</i>.

### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

The size of the font file reference key in bytes.

### -param fontFileLoader

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>*</b>

The font file loader that will be used by the font system to load data from the file identified by
     <i>fontFileReferenceKey</i>.

### -param fontFile [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

Contains an address of a pointer to the newly created font file object when this method succeeds, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 This function is provided for cases when an application or a document needs to use a private font
     without having to install it on the system. <i>fontFileReferenceKey</i> has to be unique only in the scope
     of the <i>fontFileLoader</i> used in this call.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

