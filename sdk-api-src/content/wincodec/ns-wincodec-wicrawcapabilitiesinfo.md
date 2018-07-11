---
UID: NS:wincodec.WICRawCapabilitiesInfo
title: WICRawCapabilitiesInfo
author: windows-sdk-content
description: Defines raw codec capabilites.
old-location: wic\_wic_codec_wicrawcapabilitiesinfo.htm
old-project: wic
ms.assetid: 1466cd90-8eab-4c5c-bb77-c75d35fe586b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: WICRawCapabilitiesInfo, WICRawCapabilitiesInfo structure [Windows Imaging Component], _wic_codec_wicrawcapabilitiesinfo, wic._wic_codec_wicrawcapabilitiesinfo, wincodec/WICRawCapabilitiesInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICRawCapabilitiesInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICRawCapabilitiesInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICRawCapabilitiesInfo structure


## -description


Defines raw codec capabilites.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

Size of the <b>WICRawCapabilitiesInfo</b> structure.


### -field CodecMajorVersion

Type: <b>UINT</b>

The codec's major version.


### -field CodecMinorVersion

Type: <b>UINT</b>

The codec's minor version.


### -field ExposureCompensationSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of exposure compensation support.


### -field ContrastSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of contrast support.


### -field RGBWhitePointSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of RGB white point support.


### -field NamedWhitePointSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of <a href="https://msdn.microsoft.com/e256a6d6-a035-47c3-a82c-d9aec284de17">WICNamedWhitePoint</a> support.


### -field NamedWhitePointSupportMask

Type: <b>UINT</b>

The <a href="https://msdn.microsoft.com/e256a6d6-a035-47c3-a82c-d9aec284de17">WICNamedWhitePoint</a> mask.


### -field KelvinWhitePointSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of kelvin white point support.


### -field GammaSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of gamma support.


### -field TintSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of tint support.


### -field SaturationSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of saturation support.


### -field SharpnessSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of sharpness support.


### -field NoiseReductionSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of noise reduction support.


### -field DestinationColorProfileSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of destination color profile support.


### -field ToneCurveSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of tone curve support.


### -field RotationSupport

Type: <b><a href="https://msdn.microsoft.com/f6713652-7d38-4ac6-80d8-fd53095c50a2">WICRawRotationCapabilities</a></b>

The <a href="https://msdn.microsoft.com/f6713652-7d38-4ac6-80d8-fd53095c50a2">WICRawRotationCapabilities</a> of rotation support.


### -field RenderModeSupport

Type: <b><a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a></b>

The <a href="https://msdn.microsoft.com/a82edbbe-a069-4ba8-ba15-524830cdf330">WICRawCapabilities</a> of <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a> support.

