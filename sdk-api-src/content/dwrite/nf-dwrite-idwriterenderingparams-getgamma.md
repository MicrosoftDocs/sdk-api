---
UID: NF:dwrite.IDWriteRenderingParams.GetGamma
title: IDWriteRenderingParams::GetGamma (dwrite.h)
description: Gets the gamma value used for gamma correction. Valid values must be greater than zero and cannot exceed 256.
helpviewer_keywords: ["GetGamma","GetGamma method [Direct Write]","GetGamma method [Direct Write]","IDWriteRenderingParams interface","IDWriteRenderingParams interface [Direct Write]","GetGamma method","IDWriteRenderingParams.GetGamma","IDWriteRenderingParams::GetGamma","directwrite.IDWriteRenderingParams_GetGamma","dwrite/IDWriteRenderingParams::GetGamma"]
old-location: directwrite\IDWriteRenderingParams_GetGamma.htm
tech.root: DirectWrite
ms.assetid: f83adfd6-055d-4b73-89a8-e0fe5af0b661
ms.date: 12/05/2018
ms.keywords: GetGamma, GetGamma method [Direct Write], GetGamma method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetGamma method, IDWriteRenderingParams.GetGamma, IDWriteRenderingParams::GetGamma, directwrite.IDWriteRenderingParams_GetGamma, dwrite/IDWriteRenderingParams::GetGamma
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
 - IDWriteRenderingParams::GetGamma
 - dwrite/IDWriteRenderingParams::GetGamma
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
 - IDWriteRenderingParams.GetGamma
---

# IDWriteRenderingParams::GetGamma


## -description

Gets the gamma value used for gamma correction. Valid values must be
     greater than zero and cannot exceed 256.



## -returns

Type: <b>FLOAT</b>

Returns the gamma value used for gamma correction. Valid values must be
     greater than zero and cannot exceed 256.

## -remarks

The gamma value is used for gamma correction, which compensates for the non-linear luminosity response of most monitors.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>

