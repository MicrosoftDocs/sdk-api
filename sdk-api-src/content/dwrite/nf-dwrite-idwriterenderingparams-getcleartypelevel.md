---
UID: NF:dwrite.IDWriteRenderingParams.GetClearTypeLevel
title: IDWriteRenderingParams::GetClearTypeLevel (dwrite.h)
description: Gets the ClearType level of the rendering parameters object.
helpviewer_keywords: ["GetClearTypeLevel","GetClearTypeLevel method [Direct Write]","GetClearTypeLevel method [Direct Write]","IDWriteRenderingParams interface","IDWriteRenderingParams interface [Direct Write]","GetClearTypeLevel method","IDWriteRenderingParams.GetClearTypeLevel","IDWriteRenderingParams::GetClearTypeLevel","directwrite.IDWriteRenderingParams_GetClearTypeLevel","dwrite/IDWriteRenderingParams::GetClearTypeLevel"]
old-location: directwrite\IDWriteRenderingParams_GetClearTypeLevel.htm
tech.root: DirectWrite
ms.assetid: 62b2aa39-ca8f-4abd-af10-1c1ca7971dcd
ms.date: 12/05/2018
ms.keywords: GetClearTypeLevel, GetClearTypeLevel method [Direct Write], GetClearTypeLevel method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetClearTypeLevel method, IDWriteRenderingParams.GetClearTypeLevel, IDWriteRenderingParams::GetClearTypeLevel, directwrite.IDWriteRenderingParams_GetClearTypeLevel, dwrite/IDWriteRenderingParams::GetClearTypeLevel
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
 - IDWriteRenderingParams::GetClearTypeLevel
 - dwrite/IDWriteRenderingParams::GetClearTypeLevel
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
 - IDWriteRenderingParams.GetClearTypeLevel
---

# IDWriteRenderingParams::GetClearTypeLevel


## -description

Gets the ClearType level of the rendering parameters object.



## -returns

Type: <b>FLOAT</b>

The ClearType level of the rendering parameters object.

## -remarks

The ClearType level represents the amount of ClearType – that is, the degree to which the red, green, and blue subpixels of each pixel are treated differently. Valid values range from zero (meaning no ClearType, which is equivalent to grayscale anti-aliasing) to one (meaning full ClearType)

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>

