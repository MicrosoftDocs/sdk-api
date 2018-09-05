---
UID: NF:dwrite_2.IDWriteFontFace2.GetRecommendedRenderingMode
title: IDWriteFontFace2::GetRecommendedRenderingMode
author: windows-sdk-content
description: Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.
old-location: directwrite\idwritefontface2_getrecommendedrenderingmode.htm
old-project: DirectWrite
ms.assetid: 351E9A18-CD14-421F-931F-7F25FBCA6B83
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetRecommendedRenderingMode, GetRecommendedRenderingMode method [Direct Write], GetRecommendedRenderingMode method [Direct Write],IDWriteFontFace2 interface, IDWriteFontFace2 interface [Direct Write],GetRecommendedRenderingMode method, IDWriteFontFace2.GetRecommendedRenderingMode, IDWriteFontFace2::GetRecommendedRenderingMode, directwrite.idwritefontface2_getrecommendedrenderingmode, dwrite_2/IDWriteFontFace2::GetRecommendedRenderingMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace2.GetRecommendedRenderingMode
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFace2::GetRecommendedRenderingMode


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

Type: <b><a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a>-typed value for the recommended rendering mode.


### -param gridFitMode [out]

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>-typed value for the recommended grid-fit mode.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D74F6472-CEEC-4DF5-83C8-0D65923C8028">IDWriteFontFace2</a>
 

 

