---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

