---
UID: NF:dwrite.IDWriteRenderingParams.GetEnhancedContrast
title: IDWriteRenderingParams::GetEnhancedContrast (dwrite.h)
description: Gets the enhanced contrast property of the rendering parameters object. Valid values are greater than or equal to zero.
helpviewer_keywords: ["GetEnhancedContrast","GetEnhancedContrast method [Direct Write]","GetEnhancedContrast method [Direct Write]","IDWriteRenderingParams interface","IDWriteRenderingParams interface [Direct Write]","GetEnhancedContrast method","IDWriteRenderingParams.GetEnhancedContrast","IDWriteRenderingParams::GetEnhancedContrast","directwrite.IDWriteRenderingParams_GetEnhancedContrast","dwrite/IDWriteRenderingParams::GetEnhancedContrast"]
old-location: directwrite\IDWriteRenderingParams_GetEnhancedContrast.htm
tech.root: DirectWrite
ms.assetid: dabce803-4989-4532-bf96-2f7eb09b29fe
ms.date: 12/05/2018
ms.keywords: GetEnhancedContrast, GetEnhancedContrast method [Direct Write], GetEnhancedContrast method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetEnhancedContrast method, IDWriteRenderingParams.GetEnhancedContrast, IDWriteRenderingParams::GetEnhancedContrast, directwrite.IDWriteRenderingParams_GetEnhancedContrast, dwrite/IDWriteRenderingParams::GetEnhancedContrast
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
 - IDWriteRenderingParams::GetEnhancedContrast
 - dwrite/IDWriteRenderingParams::GetEnhancedContrast
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
 - IDWriteRenderingParams.GetEnhancedContrast
---

# IDWriteRenderingParams::GetEnhancedContrast


## -description

Gets the enhanced contrast property of the rendering parameters object. Valid values are greater than or equal to zero.



## -returns

Type: <b>FLOAT</b>

Returns the amount of contrast enhancement. Valid values are greater than
     or equal to zero.

## -remarks

Enhanced contrast is the amount to increase the darkness of text, and typically ranges from 0 to 1. Zero means no contrast enhancement.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>

