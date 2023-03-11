---
UID: NF:dwrite.IDWriteLocalizedStrings.GetLocaleNameLength
title: IDWriteLocalizedStrings::GetLocaleNameLength (dwrite.h)
description: Gets the length in characters (not including the null terminator) of the locale name with the specified index. (IDWriteLocalizedStrings.GetLocaleNameLength)
helpviewer_keywords: ["GetLocaleNameLength","GetLocaleNameLength method [Direct Write]","GetLocaleNameLength method [Direct Write]","IDWriteLocalizedStrings interface","IDWriteLocalizedStrings interface [Direct Write]","GetLocaleNameLength method","IDWriteLocalizedStrings.GetLocaleNameLength","IDWriteLocalizedStrings::GetLocaleNameLength","directwrite.IDWriteLocalizedStrings_GetLocaleNameLength","dwrite/IDWriteLocalizedStrings::GetLocaleNameLength"]
old-location: directwrite\IDWriteLocalizedStrings_GetLocaleNameLength.htm
tech.root: DirectWrite
ms.assetid: a175380b-1109-476d-8bd7-9ba0753c125f
ms.date: 12/05/2018
ms.keywords: GetLocaleNameLength, GetLocaleNameLength method [Direct Write], GetLocaleNameLength method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetLocaleNameLength method, IDWriteLocalizedStrings.GetLocaleNameLength, IDWriteLocalizedStrings::GetLocaleNameLength, directwrite.IDWriteLocalizedStrings_GetLocaleNameLength, dwrite/IDWriteLocalizedStrings::GetLocaleNameLength
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
 - IDWriteLocalizedStrings::GetLocaleNameLength
 - dwrite/IDWriteLocalizedStrings::GetLocaleNameLength
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
 - IDWriteLocalizedStrings.GetLocaleNameLength
---

# IDWriteLocalizedStrings::GetLocaleNameLength


## -description

 Gets the length in characters (not including the null terminator) of the locale name with the specified index.

## -parameters

### -param index

Type: <b>UINT32</b>

Zero-based index of the locale name to be retrieved.

### -param length [out]

Type: <b>UINT32*</b>

When this method returns, contains the length in characters of the locale name, not including the null terminator.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>

