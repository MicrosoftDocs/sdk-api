---
UID: NF:dwrite.IDWriteTypography.GetFontFeature
title: IDWriteTypography::GetFontFeature (dwrite.h)
description: Gets the font feature at the specified index.
helpviewer_keywords: ["GetFontFeature","GetFontFeature method [Direct Write]","GetFontFeature method [Direct Write]","IDWriteTypography interface","IDWriteTypography interface [Direct Write]","GetFontFeature method","IDWriteTypography.GetFontFeature","IDWriteTypography::GetFontFeature","directwrite.IDWriteTypography_GetFontFeature","dwrite/IDWriteTypography::GetFontFeature"]
old-location: directwrite\IDWriteTypography_GetFontFeature.htm
tech.root: DirectWrite
ms.assetid: deb6b466-a654-4bc7-863c-9db32aa4c036
ms.date: 12/05/2018
ms.keywords: GetFontFeature, GetFontFeature method [Direct Write], GetFontFeature method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],GetFontFeature method, IDWriteTypography.GetFontFeature, IDWriteTypography::GetFontFeature, directwrite.IDWriteTypography_GetFontFeature, dwrite/IDWriteTypography::GetFontFeature
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
 - IDWriteTypography::GetFontFeature
 - dwrite/IDWriteTypography::GetFontFeature
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
 - IDWriteTypography.GetFontFeature
---

# IDWriteTypography::GetFontFeature


## -description

 Gets the font feature at the specified index.

## -parameters

### -param fontFeatureIndex

Type: <b>UINT32</b>

The zero-based index of the font feature to retrieve.

### -param fontFeature [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature">DWRITE_FONT_FEATURE</a>*</b>

When this method returns, contains the font feature which is at the specified index.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A single run of text can be associated with more than one typographic feature. The <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a> object holds a list of these font features.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a>

