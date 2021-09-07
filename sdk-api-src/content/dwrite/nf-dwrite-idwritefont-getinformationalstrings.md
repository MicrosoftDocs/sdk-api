---
UID: NF:dwrite.IDWriteFont.GetInformationalStrings
title: IDWriteFont::GetInformationalStrings (dwrite.h)
description: Gets a localized strings collection containing the specified informational strings, indexed by locale name.
helpviewer_keywords: ["GetInformationalStrings","GetInformationalStrings method [Direct Write]","GetInformationalStrings method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","GetInformationalStrings method","IDWriteFont.GetInformationalStrings","IDWriteFont::GetInformationalStrings","directwrite.IDWriteFont_GetInformationalStrings","dwrite/IDWriteFont::GetInformationalStrings"]
old-location: directwrite\IDWriteFont_GetInformationalStrings.htm
tech.root: DirectWrite
ms.assetid: a23fec10-4027-45eb-9c29-01df385b24e7
ms.date: 12/05/2018
ms.keywords: GetInformationalStrings, GetInformationalStrings method [Direct Write], GetInformationalStrings method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetInformationalStrings method, IDWriteFont.GetInformationalStrings, IDWriteFont::GetInformationalStrings, directwrite.IDWriteFont_GetInformationalStrings, dwrite/IDWriteFont::GetInformationalStrings
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
 - IDWriteFont::GetInformationalStrings
 - dwrite/IDWriteFont::GetInformationalStrings
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
 - IDWriteFont.GetInformationalStrings
---

# IDWriteFont::GetInformationalStrings


## -description

 Gets a localized strings collection containing the specified informational strings, indexed by locale name.

## -parameters

### -param informationalStringID

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id">DWRITE_INFORMATIONAL_STRING_ID</a></b>

A value that identifies the  informational string to get. For example, <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id">DWRITE_INFORMATIONAL_STRING_DESCRIPTION</a> specifies a string that contains a description of the font.

### -param informationalStrings [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

When this method returns, contains an address of a pointer to the newly created localized strings object.

### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the font contains the specified string ID; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If the font does not contain the string specified by <i>informationalStringID</i>, the return value is <b>S_OK</b> but 
     <i>informationalStrings</i> receives a <b>NULL</b> pointer and <i>exists</i> receives the value <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>

