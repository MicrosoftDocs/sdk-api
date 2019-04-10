---
UID: NF:dwrite_1.IDWriteFontFace1.GetGdiCompatibleMetrics
title: IDWriteFontFace1::GetGdiCompatibleMetrics (dwrite_1.h)
author: windows-sdk-content
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.
old-location: directwrite\idwritefontface1_getgdicompatiblemetrics.htm
tech.root: DirectWrite
ms.assetid: 2FD26970-8CF3-453F-A08D-30CC4A820281
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGdiCompatibleMetrics, GetGdiCompatibleMetrics method [Direct Write], GetGdiCompatibleMetrics method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetGdiCompatibleMetrics method, IDWriteFontFace1.GetGdiCompatibleMetrics, IDWriteFontFace1::GetGdiCompatibleMetrics, directwrite.idwritefontface1_getgdicompatiblemetrics, dwrite_1/IDWriteFontFace1::GetGdiCompatibleMetrics
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetGdiCompatibleMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace1::GetGdiCompatibleMetrics


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


### -param fontMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/F06033F4-2312-48C2-AF70-BDB83700B4E0">DWRITE_FONT_METRICS1</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/F06033F4-2312-48C2-AF70-BDB83700B4E0">DWRITE_FONT_METRICS1</a> structure to fill in. The metrics returned by this function are in font design units.


## -returns



Type: <b>HRESULT</b>

Standard HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>



<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>
 

 

