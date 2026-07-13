---
UID: NF:dwrite.IDWriteFont.GetFaceNames
title: IDWriteFont::GetFaceNames (dwrite.h)
description: Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.
helpviewer_keywords: ["GetFaceNames","GetFaceNames method [Direct Write]","GetFaceNames method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","GetFaceNames method","IDWriteFont.GetFaceNames","IDWriteFont::GetFaceNames","directwrite.IDWriteFont_GetFaceNames","dwrite/IDWriteFont::GetFaceNames"]
old-location: directwrite\IDWriteFont_GetFaceNames.htm
tech.root: DirectWrite
ms.assetid: 6475610a-68f0-4568-9d47-c83515dfa761
ms.date: 12/05/2018
ms.keywords: GetFaceNames, GetFaceNames method [Direct Write], GetFaceNames method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetFaceNames method, IDWriteFont.GetFaceNames, IDWriteFont::GetFaceNames, directwrite.IDWriteFont_GetFaceNames, dwrite/IDWriteFont::GetFaceNames
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
 - IDWriteFont::GetFaceNames
 - dwrite/IDWriteFont::GetFaceNames
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
 - IDWriteFont.GetFaceNames
---

# IDWriteFont::GetFaceNames


## -description

 Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.

## -parameters

### -param names [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

When this method returns, contains an address to a  pointer to the newly created localized strings object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>

