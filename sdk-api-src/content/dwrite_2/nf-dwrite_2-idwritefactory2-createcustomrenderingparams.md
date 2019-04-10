---
UID: NF:dwrite_2.IDWriteFactory2.CreateCustomRenderingParams
title: IDWriteFactory2::CreateCustomRenderingParams (dwrite_2.h)
author: windows-sdk-content
description: Creates a rendering parameters object with the specified properties.
old-location: directwrite\idwritefactory2_createcustomrenderingparams.htm
tech.root: DirectWrite
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory2 interface, IDWriteFactory2 interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory2.CreateCustomRenderingParams, IDWriteFactory2::CreateCustomRenderingParams, directwrite.idwritefactory2_createcustomrenderingparams, dwrite_2/IDWriteFactory2::CreateCustomRenderingParams
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteFactory2.CreateCustomRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory2::CreateCustomRenderingParams


## -description


Creates a rendering parameters object with the specified properties.


## -parameters




### -param gamma

Type: <b>FLOAT</b>

The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.


### -param enhancedContrast

Type: <b>FLOAT</b>

The amount of contrast enhancement, zero or greater.


### -param grayscaleEnhancedContrast

Type: <b>FLOAT</b>

The amount of contrast enhancement, zero or greater.


### -param clearTypeLevel

Type: <b>FLOAT</b>

The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).


### -param pixelGeometry

Type: <b><a href="https://msdn.microsoft.com/de84b37b-bcb1-432c-8876-d84eaa0e30e0">DWRITE_PIXEL_GEOMETRY</a></b>

The geometry of a device pixel.


### -param renderingMode

Type: <b><a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a></b>

Method of rendering glyphs. In most cases, this should be DWRITE_RENDERING_MODE_DEFAULT to automatically use an appropriate mode.


### -param gridFitMode

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a></b>

How to grid fit glyph outlines. In most cases, this should be DWRITE_GRID_FIT_DEFAULT to automatically choose an appropriate mode.


### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/0ABE2EBD-E568-4485-9B38-BA0E1E8FDA6F">IDWriteRenderingParams2</a>**</b>

Holds the newly created rendering parameters object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE">IDWriteFactory2</a>
 

 

