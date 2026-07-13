---
UID: NF:dwrite.IDWriteFontCollection.FindFamilyName
title: IDWriteFontCollection::FindFamilyName (dwrite.h)
description: Finds the font family with the specified family name.
helpviewer_keywords: ["FindFamilyName","FindFamilyName method [Direct Write]","FindFamilyName method [Direct Write]","IDWriteFontCollection interface","IDWriteFontCollection interface [Direct Write]","FindFamilyName method","IDWriteFontCollection.FindFamilyName","IDWriteFontCollection::FindFamilyName","directwrite.IDWriteFontCollection_FindFamilyName","dwrite/IDWriteFontCollection::FindFamilyName"]
old-location: directwrite\IDWriteFontCollection_FindFamilyName.htm
tech.root: DirectWrite
ms.assetid: 5537988f-aba0-4477-be01-72a5f8e66395
ms.date: 12/05/2018
ms.keywords: FindFamilyName, FindFamilyName method [Direct Write], FindFamilyName method [Direct Write],IDWriteFontCollection interface, IDWriteFontCollection interface [Direct Write],FindFamilyName method, IDWriteFontCollection.FindFamilyName, IDWriteFontCollection::FindFamilyName, directwrite.IDWriteFontCollection_FindFamilyName, dwrite/IDWriteFontCollection::FindFamilyName
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
 - IDWriteFontCollection::FindFamilyName
 - dwrite/IDWriteFontCollection::FindFamilyName
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
 - IDWriteFontCollection.FindFamilyName
---

# IDWriteFontCollection::FindFamilyName


## -description

 Finds the font family with the specified family name.

## -parameters

### -param familyName [in]

Type: <b>const WCHAR*</b>

An array of characters, which is null-terminated, containing the name of the font family. The name is not case-sensitive but must otherwise exactly match a family name in the collection.

### -param index [out]

Type: <b>UINT32*</b>

When this method returns, contains the zero-based index of the matching font family if the family name was found; otherwise, <b>UINT_MAX</b>.

### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the family name exists; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>

