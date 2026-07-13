---
UID: NF:dwrite_3.IDWriteStringList.GetLocaleNameLength
title: IDWriteStringList::GetLocaleNameLength (dwrite_3.h)
description: Gets the length in characters (not including the null terminator) of the locale name with the specified index. (IDWriteStringList.GetLocaleNameLength)
helpviewer_keywords: ["GetLocaleNameLength","GetLocaleNameLength method [Direct Write]","GetLocaleNameLength method [Direct Write]","IDWriteStringList interface","IDWriteStringList interface [Direct Write]","GetLocaleNameLength method","IDWriteStringList.GetLocaleNameLength","IDWriteStringList::GetLocaleNameLength","directwrite.idwritestringlist_getlocalenamelength","dwrite_3/IDWriteStringList::GetLocaleNameLength"]
old-location: directwrite\idwritestringlist_getlocalenamelength.htm
tech.root: DirectWrite
ms.assetid: AB3CDFB6-8B3E-47B1-BB19-C22E0D8D2D5C
ms.date: 09/10/2025
ms.keywords: GetLocaleNameLength, GetLocaleNameLength method [Direct Write], GetLocaleNameLength method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetLocaleNameLength method, IDWriteStringList.GetLocaleNameLength, IDWriteStringList::GetLocaleNameLength, directwrite.idwritestringlist_getlocalenamelength, dwrite_3/IDWriteStringList::GetLocaleNameLength
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
 - IDWriteStringList::GetLocaleNameLength
 - dwrite_3/IDWriteStringList::GetLocaleNameLength
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
 - IDWriteStringList.GetLocaleNameLength
---

# IDWriteStringList::GetLocaleNameLength


## -description

Gets the length in characters (not including the null terminator) of the locale name with the specified index.

## -parameters

### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the locale name.

### -param length [out]

Type: <b>UINT32*</b>

Receives the length in characters, not including the null terminator.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist">IDWriteStringList</a>

