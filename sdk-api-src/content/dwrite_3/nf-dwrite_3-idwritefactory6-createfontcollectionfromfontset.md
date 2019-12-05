---
UID: NF:dwrite_3.IDWriteFactory6.CreateFontCollectionFromFontSet
title: IDWriteFactory6::CreateFontCollectionFromFontSet
description: From a font set, create a collection of fonts grouped into families.
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateFontCollectionFromFontSet method, IDWriteFactory6.CreateFontCollectionFromFontSet, IDWriteFactory6::CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet method [Direct Write], CreateFontCollectionFromFontSet method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createfontcollectionfromfontset, dwrite_3/IDWriteFactory6::CreateFontCollectionFromFontSet
ms.topic: method
f1_keywords:
- dwrite_3/IDWriteFactory6.CreateFontCollectionFromFontSet
dev_langs:
- c++
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dwrite.lib
- Dwrite.dll
api_name:
- IDWriteFactory6::CreateFontCollectionFromFontSet
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

From a font set, create a collection of fonts grouped into families.

## -parameters

### -param fontSet

Type: **[IDWriteFontSet](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)\***

A set of fonts to use to build the collection.

### -param fontFamilyModel

Type: **[DWRITE_FONT_FAMILY_MODEL](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model)**

How to group families in the collection.

### -param fontCollection [out]

Type: **[IDWriteFontCollection2](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2)\*\***

The address of a pointer to an [IDWriteFontCollection2](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) interface. On successful completion, the function sets the pointer to a newly created font collection object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
