---
UID: NF:dwrite_3.IDWriteStringList.GetStringLength
title: IDWriteStringList::GetStringLength (dwrite_3.h)
description: Gets the length in characters (not including the null terminator) of the string with the specified index. (IDWriteStringList.GetStringLength)
helpviewer_keywords: ["GetStringLength","GetStringLength method [Direct Write]","GetStringLength method [Direct Write]","IDWriteStringList interface","IDWriteStringList interface [Direct Write]","GetStringLength method","IDWriteStringList.GetStringLength","IDWriteStringList::GetStringLength","directwrite.idwritestringlist_getstringlength","dwrite_3/IDWriteStringList::GetStringLength"]
old-location: directwrite\idwritestringlist_getstringlength.htm
tech.root: DirectWrite
ms.assetid: 5511DD28-22B1-4006-A724-13C2C4A17E6C
ms.date: 09/10/2025
ms.keywords: GetStringLength, GetStringLength method [Direct Write], GetStringLength method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetStringLength method, IDWriteStringList.GetStringLength, IDWriteStringList::GetStringLength, directwrite.idwritestringlist_getstringlength, dwrite_3/IDWriteStringList::GetStringLength
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
 - IDWriteStringList::GetStringLength
 - dwrite_3/IDWriteStringList::GetStringLength
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
 - IDWriteStringList.GetStringLength
---

# IDWriteStringList::GetStringLength


## -description

Gets the length in characters (not including the null terminator) of the string with the specified index.

## -parameters

### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the string.

### -param length [out]

Type: <b>UINT32*</b>

Receives the length in characters of the string, not including the null terminator.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist">IDWriteStringList</a>

