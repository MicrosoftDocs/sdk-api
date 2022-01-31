---
UID: NE:wincodec.WICPngTimeProperties
title: WICPngTimeProperties (wincodec.h)
description: Specifies the Portable Network Graphics (PNG) tIME chunk metadata properties.
helpviewer_keywords: ["WICPngTimeDay","WICPngTimeHour","WICPngTimeMinute","WICPngTimeMonth","WICPngTimeProperties","WICPngTimeProperties enumeration [Windows Imaging Component]","WICPngTimeSecond","WICPngTimeYear","_wic_codec_wicpngtimeproperties","wic._wic_codec_wicpngtimeproperties","wincodec/WICPngTimeDay","wincodec/WICPngTimeHour","wincodec/WICPngTimeMinute","wincodec/WICPngTimeMonth","wincodec/WICPngTimeProperties","wincodec/WICPngTimeSecond","wincodec/WICPngTimeYear"]
old-location: wic\_wic_codec_wicpngtimeproperties.htm
tech.root: wic
ms.assetid: 202dc399-0173-4995-af74-09ee71e1dcf1
ms.date: 12/05/2018
ms.keywords: WICPngTimeDay, WICPngTimeHour, WICPngTimeMinute, WICPngTimeMonth, WICPngTimeProperties, WICPngTimeProperties enumeration [Windows Imaging Component], WICPngTimeSecond, WICPngTimeYear, _wic_codec_wicpngtimeproperties, wic._wic_codec_wicpngtimeproperties, wincodec/WICPngTimeDay, wincodec/WICPngTimeHour, wincodec/WICPngTimeMinute, wincodec/WICPngTimeMonth, wincodec/WICPngTimeProperties, wincodec/WICPngTimeSecond, wincodec/WICPngTimeYear
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
req.typenames: WICPngTimeProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPngTimeProperties
 - wincodec/WICPngTimeProperties
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
 - WICPngTimeProperties
---

# WICPngTimeProperties enumeration


## -description

Specifies the Portable Network Graphics (PNG) tIME chunk metadata properties.

## -enum-fields

### -field WICPngTimeYear:0x1

[VT_UI2] Indicates the year of the last modification.

### -field WICPngTimeMonth:0x2

[VT_UI1] Indicates the month of the last modification.

### -field WICPngTimeDay:0x3

[VT_UI1] Indicates day of the last modification.

### -field WICPngTimeHour:0x4

[VT_UI1] Indicates the hour of the last modification.

### -field WICPngTimeMinute:0x5

[VT_UI1] Indicates the minute of the last modification.

### -field WICPngTimeSecond:0x6

[VT_UI1] Indicates the second of the last modification.

### -field WICPngTimeProperties_FORCE_DWORD:0x7fffffff

