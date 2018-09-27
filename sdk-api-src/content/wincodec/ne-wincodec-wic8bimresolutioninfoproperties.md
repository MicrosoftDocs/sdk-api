---
UID: NE:wincodec.WIC8BIMResolutionInfoProperties
title: WIC8BIMResolutionInfoProperties
author: windows-sdk-content
description: Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block.
old-location: wic\_wic_codec_wic8bimresolutioninfoproperties.htm
tech.root: wic
ms.assetid: a5bb984a-290c-4dd6-8b94-b8a221e78a6b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WIC8BIMResolutionInfoHResolution, WIC8BIMResolutionInfoHResolutionUnit, WIC8BIMResolutionInfoHeightUnit, WIC8BIMResolutionInfoPString, WIC8BIMResolutionInfoProperties, WIC8BIMResolutionInfoProperties enumeration [Windows Imaging Component], WIC8BIMResolutionInfoVResolution, WIC8BIMResolutionInfoVResolutionUnit, WIC8BIMResolutionInfoWidthUnit, _wic_codec_wic8bimresolutioninfoproperties, wic._wic_codec_wic8bimresolutioninfoproperties, wincodec/WIC8BIMResolutionInfoHResolution, wincodec/WIC8BIMResolutionInfoHResolutionUnit, wincodec/WIC8BIMResolutionInfoHeightUnit, wincodec/WIC8BIMResolutionInfoPString, wincodec/WIC8BIMResolutionInfoProperties, wincodec/WIC8BIMResolutionInfoVResolution, wincodec/WIC8BIMResolutionInfoVResolutionUnit, wincodec/WIC8BIMResolutionInfoWidthUnit
ms.prod: windows
ms.technology: windows-sdk
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
 - WIC8BIMResolutionInfoProperties
product: Windows
targetos: Windows
req.typenames: WIC8BIMResolutionInfoProperties
req.redist: 
---

# WIC8BIMResolutionInfoProperties enumeration


## -description


Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block.


## -enum-fields




### -field WIC8BIMResolutionInfoPString

[VT_LPSTR] A name that identifies the 8BIM block.


### -field WIC8BIMResolutionInfoHResolution

[VT_UI4] The horizontal resolution of the image.


### -field WIC8BIMResolutionInfoHResolutionUnit

[VT_UI2] The units that the horizontal resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.


### -field WIC8BIMResolutionInfoWidthUnit

[VT_UI2] The units that the image width is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.


### -field WIC8BIMResolutionInfoVResolution

[VT_UI4] The vertical resolution of the image.


### -field WIC8BIMResolutionInfoVResolutionUnit

[VT_UI2] The units that the vertical resolution is specified in; a 1 indicates pixels per inch and a 2 indicates pixels per centimeter.


### -field WIC8BIMResolutionInfoHeightUnit

[VT_UI2] The units that the image height is specified in; a 1 indicates inches, a 2 indicates centimeters, a 3 indicates points, a 4 specifies picas, and a 5 specifies columns.


### -field WIC8BIMResolutionInfoProperties_FORCE_DWORD



