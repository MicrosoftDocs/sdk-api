---
UID: NE:wincodec.WICPngFilterOption
title: WICPngFilterOption
author: windows-sdk-content
description: Specifies the Portable Network Graphics (PNG) filters available for compression optimization.
old-location: wic\_wic_codec_wicpngfilteroption.htm
tech.root: wic
ms.assetid: 468033cf-62e8-4aef-b34f-c833df048115
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WICPngFilterAdaptive, WICPngFilterAverage, WICPngFilterNone, WICPngFilterOption, WICPngFilterOption enumeration [Windows Imaging Component], WICPngFilterPaeth, WICPngFilterSub, WICPngFilterUnspecified, WICPngFilterUp, _wic_codec_wicpngfilteroption, wic._wic_codec_wicpngfilteroption, wincodec/WICPngFilterAdaptive, wincodec/WICPngFilterAverage, wincodec/WICPngFilterNone, wincodec/WICPngFilterOption, wincodec/WICPngFilterPaeth, wincodec/WICPngFilterSub, wincodec/WICPngFilterUnspecified, wincodec/WICPngFilterUp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICPngFilterOption
product: Windows
targetos: Windows
req.typenames: WICPngFilterOption
req.redist: 
---

# WICPngFilterOption enumeration


## -description


Specifies the Portable Network Graphics (PNG) filters available for compression optimization.


## -enum-fields




### -field WICPngFilterUnspecified

Indicates an unspecified PNG filter. This enables WIC to algorithmically choose the best filtering option for the image.


### -field WICPngFilterNone

Indicates no PNG filter.


### -field WICPngFilterSub

Indicates a PNG sub filter.


### -field WICPngFilterUp

Indicates a PNG up filter.


### -field WICPngFilterAverage

Indicates a PNG average filter.


### -field WICPngFilterPaeth

Indicates a PNG paeth filter.


### -field WICPngFilterAdaptive

Indicates a PNG adaptive filter. This enables WIC to choose the best filtering mode on a per-scanline basis.


### -field WICPNGFILTEROPTION_FORCE_DWORD



