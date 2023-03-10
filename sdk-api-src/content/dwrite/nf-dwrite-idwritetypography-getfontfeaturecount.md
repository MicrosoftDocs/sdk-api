---
UID: NF:dwrite.IDWriteTypography.GetFontFeatureCount
title: IDWriteTypography::GetFontFeatureCount (dwrite.h)
description: Gets the number of OpenType font features for the current font.
helpviewer_keywords: ["GetFontFeatureCount","GetFontFeatureCount method [Direct Write]","GetFontFeatureCount method [Direct Write]","IDWriteTypography interface","IDWriteTypography interface [Direct Write]","GetFontFeatureCount method","IDWriteTypography.GetFontFeatureCount","IDWriteTypography::GetFontFeatureCount","directwrite.IDWriteTypography_GetFontFeatureCount","dwrite/IDWriteTypography::GetFontFeatureCount"]
old-location: directwrite\IDWriteTypography_GetFontFeatureCount.htm
tech.root: DirectWrite
ms.assetid: 434ea913-00c9-4051-b13c-68f9d67ebd84
ms.date: 12/05/2018
ms.keywords: GetFontFeatureCount, GetFontFeatureCount method [Direct Write], GetFontFeatureCount method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],GetFontFeatureCount method, IDWriteTypography.GetFontFeatureCount, IDWriteTypography::GetFontFeatureCount, directwrite.IDWriteTypography_GetFontFeatureCount, dwrite/IDWriteTypography::GetFontFeatureCount
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
 - IDWriteTypography::GetFontFeatureCount
 - dwrite/IDWriteTypography::GetFontFeatureCount
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
 - IDWriteTypography.GetFontFeatureCount
---

# IDWriteTypography::GetFontFeatureCount


## -description

 Gets the number of OpenType font features for the current font.



## -returns

Type: <b>UINT32</b>

The number of font features for the current text format.

## -remarks

A single run of text can be associated with more than one typographic feature. The <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a> object holds a list of these font features.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a>

