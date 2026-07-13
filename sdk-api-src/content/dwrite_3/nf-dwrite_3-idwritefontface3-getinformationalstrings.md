---
UID: NF:dwrite_3.IDWriteFontFace3.GetInformationalStrings
title: IDWriteFontFace3::GetInformationalStrings (dwrite_3.h)
description: Gets a localized strings collection that contains the specified informational strings, indexed by locale name.
helpviewer_keywords: ["GetInformationalStrings","GetInformationalStrings method [Direct Write]","GetInformationalStrings method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","GetInformationalStrings method","IDWriteFontFace3.GetInformationalStrings","IDWriteFontFace3::GetInformationalStrings","directwrite.idwritefontface3_getinformationalstrings","dwrite_3/IDWriteFontFace3::GetInformationalStrings"]
old-location: directwrite\idwritefontface3_getinformationalstrings.htm
tech.root: DirectWrite
ms.assetid: F3CF5E9E-C0EA-4A29-8D42-11873DF5A9F2
ms.date: 09/10/2025
ms.keywords: GetInformationalStrings, GetInformationalStrings method [Direct Write], GetInformationalStrings method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetInformationalStrings method, IDWriteFontFace3.GetInformationalStrings, IDWriteFontFace3::GetInformationalStrings, directwrite.idwritefontface3_getinformationalstrings, dwrite_3/IDWriteFontFace3::GetInformationalStrings
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
 - IDWriteFontFace3::GetInformationalStrings
 - dwrite_3/IDWriteFontFace3::GetInformationalStrings
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
 - IDWriteFontFace3.GetInformationalStrings
---

# IDWriteFontFace3::GetInformationalStrings


## -description

Gets a localized strings collection that contains the specified informational strings, indexed by locale name.

## -parameters

### -param informationalStringID [in]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id">DWRITE_INFORMATIONAL_STRING_ID</a></b>

A <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id">DWRITE_INFORMATIONAL_STRING_ID</a>-typed value that identifies the strings to get.

### -param informationalStrings [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a> interface for the newly created localized strings object.

### -param exists [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives whether the font contains the specified string ID. <b>TRUE</b> if the font contains the specified string ID; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If the font doesn't contain the specified string, the return value is S_OK, but <i>informationalStrings</i> receives a <b>NULL</b> pointer and <i>exists</i> receives the value <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

