---
UID: NF:dwrite_3.IDWriteStringList.GetLocaleName
title: IDWriteStringList::GetLocaleName (dwrite_3.h)
description: Copies the locale name with the specified index to the specified array. (IDWriteStringList.GetLocaleName)
helpviewer_keywords: ["GetLocaleName","GetLocaleName method [Direct Write]","GetLocaleName method [Direct Write]","IDWriteStringList interface","IDWriteStringList interface [Direct Write]","GetLocaleName method","IDWriteStringList.GetLocaleName","IDWriteStringList::GetLocaleName","directwrite.idwritestringlist_getlocalename","dwrite_3/IDWriteStringList::GetLocaleName"]
old-location: directwrite\idwritestringlist_getlocalename.htm
tech.root: DirectWrite
ms.assetid: 3CB369A4-D1FC-4C8B-BE41-33D176117133
ms.date: 09/10/2025
ms.keywords: GetLocaleName, GetLocaleName method [Direct Write], GetLocaleName method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetLocaleName method, IDWriteStringList.GetLocaleName, IDWriteStringList::GetLocaleName, directwrite.idwritestringlist_getlocalename, dwrite_3/IDWriteStringList::GetLocaleName
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
 - IDWriteStringList::GetLocaleName
 - dwrite_3/IDWriteStringList::GetLocaleName
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
 - IDWriteStringList.GetLocaleName
---

# IDWriteStringList::GetLocaleName


## -description

Copies the locale name with the specified index to the specified array.

## -parameters

### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the locale name.

### -param localeName [out]

Type: <b>WCHAR*</b>

Character array that receives the locale name.

### -param size

Type: <b>UINT32</b>

Size of the array in characters. The size must include space for the terminating null character.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist">IDWriteStringList</a>

