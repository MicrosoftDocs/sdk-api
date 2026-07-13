---
UID: NF:dwrite_3.IDWriteStringList.GetString
title: IDWriteStringList::GetString (dwrite_3.h)
description: Copies the string with the specified index to the specified array. (IDWriteStringList.GetString)
helpviewer_keywords: ["GetString","GetString method [Direct Write]","GetString method [Direct Write]","IDWriteStringList interface","IDWriteStringList interface [Direct Write]","GetString method","IDWriteStringList.GetString","IDWriteStringList::GetString","directwrite.idwritestringlist_getstring","dwrite_3/IDWriteStringList::GetString"]
old-location: directwrite\idwritestringlist_getstring.htm
tech.root: DirectWrite
ms.assetid: 9F569418-F5CF-4280-8E53-32F14AE6FD42
ms.date: 09/10/2025
ms.keywords: GetString, GetString method [Direct Write], GetString method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetString method, IDWriteStringList.GetString, IDWriteStringList::GetString, directwrite.idwritestringlist_getstring, dwrite_3/IDWriteStringList::GetString
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
 - IDWriteStringList::GetString
 - dwrite_3/IDWriteStringList::GetString
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
 - IDWriteStringList.GetString
---

# IDWriteStringList::GetString


## -description

Copies the string with the specified index to the specified array.

## -parameters

### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the string.

### -param stringBuffer [out]

Type: <b>WCHAR*</b>

Character array that receives the string.

### -param stringBufferSize

Type: <b>UINT32</b>

Size of the array in characters. The size must include space for the terminating null character.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist">IDWriteStringList</a>

