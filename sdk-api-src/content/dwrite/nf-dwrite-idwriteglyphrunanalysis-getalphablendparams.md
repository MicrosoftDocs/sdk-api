---
UID: NF:dwrite.IDWriteGlyphRunAnalysis.GetAlphaBlendParams
title: IDWriteGlyphRunAnalysis::GetAlphaBlendParams
author: windows-sdk-content
description: Gets alpha blending properties required for ClearType blending.
old-location: directwrite\IDWriteGlyphRunAnalysis_GetAlphaBlendParams.htm
tech.root: DirectWrite
ms.assetid: 21991479-f041-40f9-83d5-0718ede26b92
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetAlphaBlendParams, GetAlphaBlendParams method [Direct Write], GetAlphaBlendParams method [Direct Write],IDWriteGlyphRunAnalysis interface, IDWriteGlyphRunAnalysis interface [Direct Write],GetAlphaBlendParams method, IDWriteGlyphRunAnalysis.GetAlphaBlendParams, IDWriteGlyphRunAnalysis::GetAlphaBlendParams, directwrite.IDWriteGlyphRunAnalysis_GetAlphaBlendParams, dwrite/IDWriteGlyphRunAnalysis::GetAlphaBlendParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteGlyphRunAnalysis.GetAlphaBlendParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGlyphRunAnalysis::GetAlphaBlendParams


## -description


 Gets alpha blending properties required for ClearType blending.


## -parameters




### -param renderingParams

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>*</b>

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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d4739b55-1a9b-4346-9b47-d8adb98df163">IDWriteGlyphRunAnalysis</a>
 

 

