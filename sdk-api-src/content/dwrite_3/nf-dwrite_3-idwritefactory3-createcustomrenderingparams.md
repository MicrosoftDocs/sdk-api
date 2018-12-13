---
UID: NF:dwrite_3.IDWriteFactory3.CreateCustomRenderingParams
title: IDWriteFactory3::CreateCustomRenderingParams
author: windows-sdk-content
description: Creates a rendering parameters object with the specified properties.
old-location: directwrite\idwritefactory3_createcustomrenderingparams.htm
tech.root: DirectWrite
ms.assetid: 60FA5675-C1E2-40CC-874D-F7E8942165CC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory3.CreateCustomRenderingParams, IDWriteFactory3::CreateCustomRenderingParams, directwrite.idwritefactory3_createcustomrenderingparams, dwrite_3/IDWriteFactory3::CreateCustomRenderingParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFactory3.CreateCustomRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::CreateCustomRenderingParams


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

The amount of contrast enhancement to use for grayscale antialiasing, zero or greater.


### -param clearTypeLevel

Type: <b>FLOAT</b>

The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).


### -param pixelGeometry

Type: <b><a href="https://msdn.microsoft.com/de84b37b-bcb1-432c-8876-d84eaa0e30e0">DWRITE_PIXEL_GEOMETRY</a></b>

A <a href="https://msdn.microsoft.com/de84b37b-bcb1-432c-8876-d84eaa0e30e0">DWRITE_PIXEL_GEOMETRY</a>-typed value that specifies the internal structure of a device pixel (that is, the physical arrangement of red, green, and blue color components) that is assumed for purposes of rendering text.
          


### -param renderingMode

Type: <b><a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a></b>

A <a href="https://msdn.microsoft.com/CAA88479-FE39-48D0-89D8-CEA0C922428A">DWRITE_RENDERING_MODE1</a>-typed value that specifies the method (for example, ClearType natural quality) for rendering glyphs. In most cases, specify <b>DWRITE_RENDERING_MODE1_DEFAULT</b> to automatically use an appropriate mode.
          


### -param gridFitMode

Type: <b><a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a></b>

A <a href="https://msdn.microsoft.com/C32A6017-3711-482B-B806-79651163DEF6">DWRITE_GRID_FIT_MODE</a>-typed value that specifies how to grid-fit glyph outlines. In most cases, specify <b>DWRITE_GRID_FIT_DEFAULT</b> to automatically choose an appropriate mode.
          


### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/A083377C-7315-40F4-AD94-9B65B98DE0D6">IDWriteRenderingParams3</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/A083377C-7315-40F4-AD94-9B65B98DE0D6">IDWriteRenderingParams3</a> interface for the newly created rendering parameters object, or <b>NULL</b> in case of failure.
          


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

