---
UID: NE:wincodec.WICNamedWhitePoint
title: WICNamedWhitePoint (wincodec.h)
description: Specifies named white balances for raw images.
helpviewer_keywords: ["WICNamedWhitePoint","WICNamedWhitePoint enumeration [Windows Imaging Component]","WICWhitePointAsShot","WICWhitePointAutoWhiteBalance","WICWhitePointCloudy","WICWhitePointCustom","WICWhitePointDaylight","WICWhitePointDefault","WICWhitePointFlash","WICWhitePointFluorescent","WICWhitePointShade","WICWhitePointTungsten","WICWhitePointUnderwater","_wic_codec_wicnamedwhitepoint","wic._wic_codec_wicnamedwhitepoint","wincodec/WICNamedWhitePoint","wincodec/WICWhitePointAsShot","wincodec/WICWhitePointAutoWhiteBalance","wincodec/WICWhitePointCloudy","wincodec/WICWhitePointCustom","wincodec/WICWhitePointDaylight","wincodec/WICWhitePointDefault","wincodec/WICWhitePointFlash","wincodec/WICWhitePointFluorescent","wincodec/WICWhitePointShade","wincodec/WICWhitePointTungsten","wincodec/WICWhitePointUnderwater"]
old-location: wic\_wic_codec_wicnamedwhitepoint.htm
tech.root: wic
ms.assetid: e256a6d6-a035-47c3-a82c-d9aec284de17
ms.date: 12/05/2018
ms.keywords: WICNamedWhitePoint, WICNamedWhitePoint enumeration [Windows Imaging Component], WICWhitePointAsShot, WICWhitePointAutoWhiteBalance, WICWhitePointCloudy, WICWhitePointCustom, WICWhitePointDaylight, WICWhitePointDefault, WICWhitePointFlash, WICWhitePointFluorescent, WICWhitePointShade, WICWhitePointTungsten, WICWhitePointUnderwater, _wic_codec_wicnamedwhitepoint, wic._wic_codec_wicnamedwhitepoint, wincodec/WICNamedWhitePoint, wincodec/WICWhitePointAsShot, wincodec/WICWhitePointAutoWhiteBalance, wincodec/WICWhitePointCloudy, wincodec/WICWhitePointCustom, wincodec/WICWhitePointDaylight, wincodec/WICWhitePointDefault, wincodec/WICWhitePointFlash, wincodec/WICWhitePointFluorescent, wincodec/WICWhitePointShade, wincodec/WICWhitePointTungsten, wincodec/WICWhitePointUnderwater
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: WICNamedWhitePoint
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICNamedWhitePoint
 - wincodec/WICNamedWhitePoint
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
 - WICNamedWhitePoint
---

# WICNamedWhitePoint enumeration


## -description

Specifies named white balances for raw images.

## -enum-fields

### -field WICWhitePointDefault:0x1

The default white balance.

### -field WICWhitePointDaylight:0x2

A daylight white balance.

### -field WICWhitePointCloudy:0x4

A cloudy white balance.

### -field WICWhitePointShade:0x8

A shade white balance.

### -field WICWhitePointTungsten:0x10

A tungsten white balance.

### -field WICWhitePointFluorescent:0x20

A fluorescent white balance.

### -field WICWhitePointFlash:0x40

Daylight white balance.

### -field WICWhitePointUnderwater:0x80

A flash white balance.

### -field WICWhitePointCustom:0x100

A custom white balance. This is typically used when using a picture (grey-card) as white balance.

### -field WICWhitePointAutoWhiteBalance:0x200

An automatic balance.

### -field WICWhitePointAsShot

An "as shot" white balance.

### -field WICNAMEDWHITEPOINT_FORCE_DWORD:0x7fffffff

