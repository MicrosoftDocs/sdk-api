---
UID: NF:dwrite.IDWriteTypography.AddFontFeature
title: IDWriteTypography::AddFontFeature (dwrite.h)
description: Adds an OpenType font feature.
helpviewer_keywords: ["AddFontFeature","AddFontFeature method [Direct Write]","AddFontFeature method [Direct Write]","IDWriteTypography interface","IDWriteTypography interface [Direct Write]","AddFontFeature method","IDWriteTypography.AddFontFeature","IDWriteTypography::AddFontFeature","directwrite.IDWriteTypography_AddFontFeature","dwrite/IDWriteTypography::AddFontFeature"]
old-location: directwrite\IDWriteTypography_AddFontFeature.htm
tech.root: DirectWrite
ms.assetid: 6d86a66d-a72f-4288-864f-90f877bd166d
ms.date: 12/05/2018
ms.keywords: AddFontFeature, AddFontFeature method [Direct Write], AddFontFeature method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],AddFontFeature method, IDWriteTypography.AddFontFeature, IDWriteTypography::AddFontFeature, directwrite.IDWriteTypography_AddFontFeature, dwrite/IDWriteTypography::AddFontFeature
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
 - IDWriteTypography::AddFontFeature
 - dwrite/IDWriteTypography::AddFontFeature
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
 - IDWriteTypography.AddFontFeature
---

# IDWriteTypography::AddFontFeature


## -description

 Adds an OpenType font feature.

## -parameters

### -param fontFeature [in]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature">DWRITE_FONT_FEATURE</a></b>

A structure that contains the OpenType name identifier and the execution parameter for the font feature being added.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a>

