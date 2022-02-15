---
UID: NF:dwrite.IDWriteRenderingParams.GetRenderingMode
title: IDWriteRenderingParams::GetRenderingMode (dwrite.h)
description: Gets the rendering mode of the rendering parameters object.
helpviewer_keywords: ["GetRenderingMode","GetRenderingMode method [Direct Write]","GetRenderingMode method [Direct Write]","IDWriteRenderingParams interface","IDWriteRenderingParams interface [Direct Write]","GetRenderingMode method","IDWriteRenderingParams.GetRenderingMode","IDWriteRenderingParams::GetRenderingMode","directwrite.IDWriteRenderingParams_GetRenderingMode","dwrite/IDWriteRenderingParams::GetRenderingMode"]
old-location: directwrite\IDWriteRenderingParams_GetRenderingMode.htm
tech.root: DirectWrite
ms.assetid: 657360c6-3351-400b-bb41-bcd92de3c48d
ms.date: 12/05/2018
ms.keywords: GetRenderingMode, GetRenderingMode method [Direct Write], GetRenderingMode method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetRenderingMode method, IDWriteRenderingParams.GetRenderingMode, IDWriteRenderingParams::GetRenderingMode, directwrite.IDWriteRenderingParams_GetRenderingMode, dwrite/IDWriteRenderingParams::GetRenderingMode
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
 - IDWriteRenderingParams::GetRenderingMode
 - dwrite/IDWriteRenderingParams::GetRenderingMode
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
 - IDWriteRenderingParams.GetRenderingMode
---

# IDWriteRenderingParams::GetRenderingMode


## -description

Gets the rendering mode of the rendering parameters object.



## -returns

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a></b>

A value that indicates the rendering mode of the rendering parameters object.

## -remarks

By default, the rendering mode is initialized to DWRITE_RENDERING_MODE_DEFAULT, which means the rendering mode is determined automatically based on the font and size. To determine the recommended rendering mode to use for a given font and size and rendering parameters object, use the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode">IDWriteFontFace::GetRecommendedRenderingMode</a> method.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>

