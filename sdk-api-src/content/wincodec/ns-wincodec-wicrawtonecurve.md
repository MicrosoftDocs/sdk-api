---
UID: NS:wincodec.WICRawToneCurve
title: WICRawToneCurve (wincodec.h)
author: windows-sdk-content
description: Represents a raw image tone curve.
old-location: wic\_wic_codec_wicrawtonecurve.htm
tech.root: wic
ms.assetid: 45eedc32-a642-4ef6-a02a-63eaeacf0012
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WICRawToneCurve, WICRawToneCurve structure [Windows Imaging Component], _wic_codec_wicrawtonecurve, wic._wic_codec_wicrawtonecurve, wincodec/WICRawToneCurve
ms.topic: struct
f1_keywords: 
 - "wincodec/WICRawToneCurve"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICRawToneCurve
targetos: Windows
req.typenames: WICRawToneCurve
req.redist: 
ms.custom: 19H1
---

# WICRawToneCurve structure


## -description


Represents a raw image tone curve.


## -struct-fields




### -field cPoints

Type: <b>UINT</b>

The number of tone curve points.


### -field aPoints

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ns-wincodec-wicrawtonecurvepoint">WICRawToneCurvePoint</a>[1]</b>

The array of tone curve points.

