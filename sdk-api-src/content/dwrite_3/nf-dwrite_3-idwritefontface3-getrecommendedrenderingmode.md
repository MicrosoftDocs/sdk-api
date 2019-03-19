---
UID: NF:dwrite_3.IDWriteFontFace3.GetRecommendedRenderingMode
title: IDWriteFontFace3::GetRecommendedRenderingMode (dwrite_3.h)
author: windows-sdk-content
description: Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.
old-location: directwrite\idwritefontface3_getrecommendedrenderingmode.htm
tech.root: DirectWrite
ms.assetid: 9EF4A414-8DD9-431B-81A6-D87F4CF9AA73
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecommendedRenderingMode, GetRecommendedRenderingMode method [Direct Write], GetRecommendedRenderingMode method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetRecommendedRenderingMode method, IDWriteFontFace3.GetRecommendedRenderingMode, IDWriteFontFace3::GetRecommendedRenderingMode, directwrite.idwritefontface3_getrecommendedrenderingmode, dwrite_3/IDWriteFontFace3::GetRecommendedRenderingMode
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3.GetRecommendedRenderingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3::GetRecommendedRenderingMode


## -description


Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.


## -parameters




### -param fontEmSize [in]

Type: <b>FLOAT</b>

Logical font size in DIPs.


### -param dpiX [in]

Type: <b>FLOAT</b>

Number of pixels per logical inch in the horizontal direction.


### -param dpiY [in]

Type: <b>FLOAT</b>

Number of pixels per logical inch in the vertical direction.


### -param transform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

A <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a> structure that describes the world transform.


### -param isSideways [in]

Type: <b>BOOL</b>

Specifies whether the font is sideways. <b>TRUE</b> if the font is sideways; otherwise, <b>FALSE</b>.




### -param outlineThreshold [in]

Type: <b><a href="https://msdn.microsoft.com/F0159E05-A47F-444E-BB07-99AA97DAC0A3">DWRITE_OUTLINE_THRESHOLD</a></b>

A <a href="https://msdn.microsoft.com/F0159E05-A47F-444E-BB07-99AA97DAC0A3">DWRITE_OUTLINE_THRESHOLD</a>-typed value that specifies the quality of the graphics system's outline rendering, affects the size threshold above which outline rendering is used.


### -param measuringMode [in]

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

A <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a>-typed value that specifies  the method used to measure during text layout. For proper glyph spacing, this method returns a rendering mode that is compatible with the specified measuring mode.


### -param renderingParams [in, optional]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a> interface for the rendering parameters object. This parameter is necessary in case the rendering parameters object overrides the rendering mode.


### -param renderingMode [out]

Type: <b><a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a>-typed value for the recommended rendering mode.


### -param gridFitMode [out]

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>-typed value for the recommended grid-fit mode.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1081A005-E4A8-4EE0-AFE0-10BD8D8471DF">IDWriteFontFace3</a>
 

 

