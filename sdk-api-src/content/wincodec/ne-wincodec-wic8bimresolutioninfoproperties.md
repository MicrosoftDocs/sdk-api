---
UID: NE:wincodec.WIC8BIMResolutionInfoProperties
title: WIC8BIMResolutionInfoProperties (wincodec.h)
description: Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block.
helpviewer_keywords: ["WIC8BIMResolutionInfoHResolution","WIC8BIMResolutionInfoHResolutionUnit","WIC8BIMResolutionInfoHeightUnit","WIC8BIMResolutionInfoPString","WIC8BIMResolutionInfoProperties","WIC8BIMResolutionInfoProperties enumeration [Windows Imaging Component]","WIC8BIMResolutionInfoVResolution","WIC8BIMResolutionInfoVResolutionUnit","WIC8BIMResolutionInfoWidthUnit","_wic_codec_wic8bimresolutioninfoproperties","wic._wic_codec_wic8bimresolutioninfoproperties","wincodec/WIC8BIMResolutionInfoHResolution","wincodec/WIC8BIMResolutionInfoHResolutionUnit","wincodec/WIC8BIMResolutionInfoHeightUnit","wincodec/WIC8BIMResolutionInfoPString","wincodec/WIC8BIMResolutionInfoProperties","wincodec/WIC8BIMResolutionInfoVResolution","wincodec/WIC8BIMResolutionInfoVResolutionUnit","wincodec/WIC8BIMResolutionInfoWidthUnit"]
old-location: wic\_wic_codec_wic8bimresolutioninfoproperties.htm
tech.root: wic
ms.assetid: a5bb984a-290c-4dd6-8b94-b8a221e78a6b
ms.date: 12/05/2018
ms.keywords: WIC8BIMResolutionInfoHResolution, WIC8BIMResolutionInfoHResolutionUnit, WIC8BIMResolutionInfoHeightUnit, WIC8BIMResolutionInfoPString, WIC8BIMResolutionInfoProperties, WIC8BIMResolutionInfoProperties enumeration [Windows Imaging Component], WIC8BIMResolutionInfoVResolution, WIC8BIMResolutionInfoVResolutionUnit, WIC8BIMResolutionInfoWidthUnit, _wic_codec_wic8bimresolutioninfoproperties, wic._wic_codec_wic8bimresolutioninfoproperties, wincodec/WIC8BIMResolutionInfoHResolution, wincodec/WIC8BIMResolutionInfoHResolutionUnit, wincodec/WIC8BIMResolutionInfoHeightUnit, wincodec/WIC8BIMResolutionInfoPString, wincodec/WIC8BIMResolutionInfoProperties, wincodec/WIC8BIMResolutionInfoVResolution, wincodec/WIC8BIMResolutionInfoVResolutionUnit, wincodec/WIC8BIMResolutionInfoWidthUnit
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
targetos: Windows
req.typenames: WIC8BIMResolutionInfoProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WIC8BIMResolutionInfoProperties
 - wincodec/WIC8BIMResolutionInfoProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WIC8BIMResolutionInfoProperties
---

# WIC8BIMResolutionInfoProperties enumeration


## -description

Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block.

## -enum-fields

### -field WIC8BIMResolutionInfoPString:0x1

[VT_LPSTR] A name that identifies the 8BIM block.

### -field WIC8BIMResolutionInfoHResolution:0x2

[VT_UI4] The horizontal resolution of the image.

### -field WIC8BIMResolutionInfoHResolutionUnit:0x3

[VT_UI2] The units that the horizontal resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.

### -field WIC8BIMResolutionInfoWidthUnit:0x4

[VT_UI2] The units that the image width is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.

### -field WIC8BIMResolutionInfoVResolution:0x5

[VT_UI4] The vertical resolution of the image.

### -field WIC8BIMResolutionInfoVResolutionUnit:0x6

[VT_UI2] The units that the vertical resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.

### -field WIC8BIMResolutionInfoHeightUnit:0x7

[VT_UI2] The units that the image height is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.

### -field WIC8BIMResolutionInfoProperties_FORCE_DWORD:0x7fffffff

