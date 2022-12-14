---
UID: NS:wincodec.WICRawCapabilitiesInfo
title: WICRawCapabilitiesInfo (wincodec.h)
description: Defines raw codec capabilities.
helpviewer_keywords: ["WICRawCapabilitiesInfo","WICRawCapabilitiesInfo structure [Windows Imaging Component]","_wic_codec_wicrawcapabilitiesinfo","wic._wic_codec_wicrawcapabilitiesinfo","wincodec/WICRawCapabilitiesInfo"]
old-location: wic\_wic_codec_wicrawcapabilitiesinfo.htm
tech.root: wic
ms.assetid: 1466cd90-8eab-4c5c-bb77-c75d35fe586b
ms.date: 12/05/2018
ms.keywords: WICRawCapabilitiesInfo, WICRawCapabilitiesInfo structure [Windows Imaging Component], _wic_codec_wicrawcapabilitiesinfo, wic._wic_codec_wicrawcapabilitiesinfo, wincodec/WICRawCapabilitiesInfo
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICRawCapabilitiesInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICRawCapabilitiesInfo
 - wincodec/WICRawCapabilitiesInfo
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
 - WICRawCapabilitiesInfo
---

# WICRawCapabilitiesInfo structure


## -description

Defines raw codec capabilities.

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

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of exposure compensation support.

### -field ContrastSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of contrast support.

### -field RGBWhitePointSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of RGB white point support.

### -field NamedWhitePointSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of <a href="/windows/desktop/api/wincodec/ne-wincodec-wicnamedwhitepoint">WICNamedWhitePoint</a> support.

### -field NamedWhitePointSupportMask

Type: <b>UINT</b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicnamedwhitepoint">WICNamedWhitePoint</a> mask.

### -field KelvinWhitePointSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of kelvin white point support.

### -field GammaSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of gamma support.

### -field TintSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of tint support.

### -field SaturationSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of saturation support.

### -field SharpnessSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of sharpness support.

### -field NoiseReductionSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of noise reduction support.

### -field DestinationColorProfileSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of destination color profile support.

### -field ToneCurveSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of tone curve support.

### -field RotationSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawrotationcapabilities">WICRawRotationCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawrotationcapabilities">WICRawRotationCapabilities</a> of rotation support.

### -field RenderModeSupport

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawcapabilities">WICRawCapabilities</a> of <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawrendermode">WICRawRenderMode</a> support.