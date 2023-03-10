---
UID: NF:dwrite.IDWriteFontCollectionLoader.CreateEnumeratorFromKey
title: IDWriteFontCollectionLoader::CreateEnumeratorFromKey (dwrite.h)
description: Creates a font file enumerator object that encapsulates a collection of font files. The font system calls back to this interface to create a font collection.
helpviewer_keywords: ["CreateEnumeratorFromKey","CreateEnumeratorFromKey method [Direct Write]","CreateEnumeratorFromKey method [Direct Write]","IDWriteFontCollectionLoader interface","IDWriteFontCollectionLoader interface [Direct Write]","CreateEnumeratorFromKey method","IDWriteFontCollectionLoader.CreateEnumeratorFromKey","IDWriteFontCollectionLoader::CreateEnumeratorFromKey","directwrite.IDWriteFontCollectionLoader_CreateEnumeratorFromKey","dwrite/IDWriteFontCollectionLoader::CreateEnumeratorFromKey"]
old-location: directwrite\IDWriteFontCollectionLoader_CreateEnumeratorFromKey.htm
tech.root: DirectWrite
ms.assetid: 579893e8-5ef3-4e23-a139-b5c203805c5c
ms.date: 12/05/2018
ms.keywords: CreateEnumeratorFromKey, CreateEnumeratorFromKey method [Direct Write], CreateEnumeratorFromKey method [Direct Write],IDWriteFontCollectionLoader interface, IDWriteFontCollectionLoader interface [Direct Write],CreateEnumeratorFromKey method, IDWriteFontCollectionLoader.CreateEnumeratorFromKey, IDWriteFontCollectionLoader::CreateEnumeratorFromKey, directwrite.IDWriteFontCollectionLoader_CreateEnumeratorFromKey, dwrite/IDWriteFontCollectionLoader::CreateEnumeratorFromKey
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
 - IDWriteFontCollectionLoader::CreateEnumeratorFromKey
 - dwrite/IDWriteFontCollectionLoader::CreateEnumeratorFromKey
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
 - IDWriteFontCollectionLoader.CreateEnumeratorFromKey
---

# IDWriteFontCollectionLoader::CreateEnumeratorFromKey


## -description

 Creates a font file enumerator object that encapsulates a collection of font files.
     The font system calls back to this interface to create a font collection.

## -parameters

### -param factory

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>*</b>

Pointer to the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a> object that was used to create the current font collection.

### -param collectionKey [in]

Type: <b>const void*</b>

A font collection key that uniquely identifies the collection of font files within
     the scope of the font collection loader being used. The buffer allocated for this key must be at least  the size, in bytes, specified by <i>collectionKeySize</i>.

### -param collectionKeySize

Type: <b>UINT32</b>

The size of the font collection key, in bytes.

### -param fontFileEnumerator [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator">IDWriteFontFileEnumerator</a>**</b>

When this method returns, contains the address of  a pointer to the newly created font file enumerator.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader">IDWriteFontCollectionLoader</a>

