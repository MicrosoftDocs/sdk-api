---
UID: NF:dwrite.IDWriteFontFace.GetGdiCompatibleMetrics
title: IDWriteFontFace::GetGdiCompatibleMetrics (dwrite.h)
author: windows-sdk-content
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.
old-location: directwrite\idwritefontface_getgdicompatiblemetrics.htm
tech.root: DirectWrite
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGdiCompatibleMetrics, GetGdiCompatibleMetrics method [Direct Write], GetGdiCompatibleMetrics method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetGdiCompatibleMetrics method, IDWriteFontFace.GetGdiCompatibleMetrics, IDWriteFontFace::GetGdiCompatibleMetrics, directwrite.idwritefontface_getgdicompatiblemetrics, dwrite/IDWriteFontFace::GetGdiCompatibleMetrics
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteFontFace.GetGdiCompatibleMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace::GetGdiCompatibleMetrics


## -description


Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.


## -parameters




### -param emSize

Type: <b>FLOAT</b>

The logical size of the font in DIP units.


### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP.


### -param transform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

An optional transform applied to the glyphs and their positions. This transform is applied after the scaling specified by the font size and <i>pixelsPerDip</i>.


### -param fontFaceMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRIC</a>S structure to fill in. The metrics returned by this function are in font design units.


## -returns



Type: <b>HRESULT</b>

Standard HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>
 

 

