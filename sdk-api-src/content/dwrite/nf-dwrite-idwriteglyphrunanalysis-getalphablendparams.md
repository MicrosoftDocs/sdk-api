---
UID: NF:dwrite.IDWriteGlyphRunAnalysis.GetAlphaBlendParams
title: IDWriteGlyphRunAnalysis::GetAlphaBlendParams (dwrite.h)
description: Gets alpha blending properties required for ClearType blending.
helpviewer_keywords: ["GetAlphaBlendParams","GetAlphaBlendParams method [Direct Write]","GetAlphaBlendParams method [Direct Write]","IDWriteGlyphRunAnalysis interface","IDWriteGlyphRunAnalysis interface [Direct Write]","GetAlphaBlendParams method","IDWriteGlyphRunAnalysis.GetAlphaBlendParams","IDWriteGlyphRunAnalysis::GetAlphaBlendParams","directwrite.IDWriteGlyphRunAnalysis_GetAlphaBlendParams","dwrite/IDWriteGlyphRunAnalysis::GetAlphaBlendParams"]
old-location: directwrite\IDWriteGlyphRunAnalysis_GetAlphaBlendParams.htm
tech.root: DirectWrite
ms.assetid: 21991479-f041-40f9-83d5-0718ede26b92
ms.date: 12/05/2018
ms.keywords: GetAlphaBlendParams, GetAlphaBlendParams method [Direct Write], GetAlphaBlendParams method [Direct Write],IDWriteGlyphRunAnalysis interface, IDWriteGlyphRunAnalysis interface [Direct Write],GetAlphaBlendParams method, IDWriteGlyphRunAnalysis.GetAlphaBlendParams, IDWriteGlyphRunAnalysis::GetAlphaBlendParams, directwrite.IDWriteGlyphRunAnalysis_GetAlphaBlendParams, dwrite/IDWriteGlyphRunAnalysis::GetAlphaBlendParams
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
 - IDWriteGlyphRunAnalysis::GetAlphaBlendParams
 - dwrite/IDWriteGlyphRunAnalysis::GetAlphaBlendParams
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
 - IDWriteGlyphRunAnalysis.GetAlphaBlendParams
---

# IDWriteGlyphRunAnalysis::GetAlphaBlendParams


## -description

 Gets alpha blending properties required for ClearType blending.

## -parameters

### -param renderingParams

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>*</b>

An object that specifies the ClearType level and enhanced contrast, gamma, pixel geometry, and rendering mode. In most cases, the values returned by the output
     parameters of this method are based on the properties of this object, unless a GDI-compatible rendering mode
     was specified.

### -param blendGamma [out]

Type: <b>FLOAT*</b>

When this method returns, contains  the gamma value to use for gamma correction.

### -param blendEnhancedContrast [out]

Type: <b>FLOAT*</b>

When this method returns, contains the enhanced contrast value to be used for blending.

### -param blendClearTypeLevel [out]

Type: <b>FLOAT*</b>

When this method returns, contains  the ClearType level used in the alpha blending.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>

