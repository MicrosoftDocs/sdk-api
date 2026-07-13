---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontCollectionFromFontSet
title: IDWriteFactory3::CreateFontCollectionFromFontSet (dwrite_3.h)
description: Create a weight/width/slope tree from a set of fonts.
helpviewer_keywords: ["CreateFontCollectionFromFontSet","CreateFontCollectionFromFontSet method [Direct Write]","CreateFontCollectionFromFontSet method [Direct Write]","IDWriteFactory3 interface","IDWriteFactory3 interface [Direct Write]","CreateFontCollectionFromFontSet method","IDWriteFactory3.CreateFontCollectionFromFontSet","IDWriteFactory3::CreateFontCollectionFromFontSet","directwrite.idwritefactory3_createfontcollectionfromfontset","dwrite_3/IDWriteFactory3::CreateFontCollectionFromFontSet"]
old-location: directwrite\idwritefactory3_createfontcollectionfromfontset.htm
tech.root: DirectWrite
ms.assetid: 22cc005f-6d34-f701-ff83-63ba819ab651
ms.date: 09/10/2025
ms.keywords: CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet method [Direct Write], CreateFontCollectionFromFontSet method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontCollectionFromFontSet method, IDWriteFactory3.CreateFontCollectionFromFontSet, IDWriteFactory3::CreateFontCollectionFromFontSet, directwrite.idwritefactory3_createfontcollectionfromfontset, dwrite_3/IDWriteFactory3::CreateFontCollectionFromFontSet
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFactory3::CreateFontCollectionFromFontSet
 - dwrite_3/IDWriteFactory3::CreateFontCollectionFromFontSet
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
 - IDWriteFactory3.CreateFontCollectionFromFontSet
---

# IDWriteFactory3::CreateFontCollectionFromFontSet


## -description

Create a weight/width/slope tree from a set of fonts.

## -parameters

### -param fontSet

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>*</b>

A set of fonts to use to build the collection.

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1">IDWriteFontCollection1</a>**</b>

Holds the newly created font collection object, or NULL in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>

