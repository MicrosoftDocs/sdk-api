---
UID: NS:dxva2api._DXVA2_VideoProcessBltParams
title: DXVA2_VideoProcessBltParams (dxva2api.h)
description: Contains parameters for the IDirectXVideoProcessor::VideoProcessBlt method.
helpviewer_keywords: ["6929fa8b-3cab-4d4e-ab2a-a3059b00905f","DXVA2_DestData_RFF","DXVA2_DestData_RFF_TFF_Present","DXVA2_DestData_TFF","DXVA2_VideoProcessBltParams","DXVA2_VideoProcessBltParams structure [Media Foundation]","dxva2api/DXVA2_VideoProcessBltParams","mf.dxva2_videoprocessbltparams"]
old-location: mf\dxva2_videoprocessbltparams.htm
tech.root: mf
ms.assetid: 6929fa8b-3cab-4d4e-ab2a-a3059b00905f
ms.date: 12/05/2018
ms.keywords: 6929fa8b-3cab-4d4e-ab2a-a3059b00905f, DXVA2_DestData_RFF, DXVA2_DestData_RFF_TFF_Present, DXVA2_DestData_TFF, DXVA2_VideoProcessBltParams, DXVA2_VideoProcessBltParams structure [Media Foundation], dxva2api/DXVA2_VideoProcessBltParams, mf.dxva2_videoprocessbltparams
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXVA2_VideoProcessBltParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoProcessBltParams
 - dxva2api/_DXVA2_VideoProcessBltParams
 - DXVA2_VideoProcessBltParams
 - dxva2api/DXVA2_VideoProcessBltParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_VideoProcessBltParams
---

# DXVA2_VideoProcessBltParams structure


## -description

Contains parameters for the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt">IDirectXVideoProcessor::VideoProcessBlt</a> method.

## -struct-fields

### -field TargetFrame

Presentation time for the target frame, in 100-nanosecond units. If the video is interlaced, this value must be either the start time for the frame or the midpoint for the frame. If the video is progressive, this value must be the start time.

### -field TargetRect

Specifies the target rectangle, which is the rectangle within the destination surface where the output video frame is drawn.
          

The target rectangle cannot be larger than the destination surface.

### -field ConstrictionSize

Size to which the output video should be downsampled. 
          If this feature is supported, the driver sets the <b>DXVA2_VideoProcess_Constriction</b> flag in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps">DXVA2_VideoProcessorCaps</a> structure.

The downsampling size cannot be less than zero, or larger than the size of the target rectangle (<b>TargetRect</b>).

### -field StreamingFlags

Reserved. Set to zero.

### -field BackgroundColor

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample16">DXVA2_AYUVSample16</a> structure that specifies the background color for the destination rectangle. The background color is used wherever no video image appears, but only within the <b>TargetRect</b> rectangle. The color is specified as an AYUV color value with 16 bits per channel. 

The alpha channel (<b>Alpha</b>) must be opaque (0xFFFF). The DXVA driver should ignore the value of the alpha channel. 

The color space for the background color is given by the <b>DestFormat</b> member. Note that the background color is always specified as a YUV color, even if the destination surface is RGB.

### -field DestFormat

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure that contains extended color information for the destination rectangle. For video playback, the recommended value for the nominal range is DXVA2_NominalRange_Unknown. For more information, see <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_nominalrange">DXVA2_NominalRange</a> enumeration.

### -field ProcAmpValues

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_procampvalues">DXVA2_ProcAmpValues</a> structure that specifies color adjustment (ProcAmp) settings. These values must fall within the ranges returned by the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getprocamprange">IDirectXVideoProcessor::GetProcAmpRange</a> method.

### -field Alpha

Alpha value that is applied to the composited image when it is copied to the destination surface. The alpha value is fixed-point value, specified as a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_fixed32">DXVA2_Fixed32</a> structure. To specify 100% opacity, use the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2_fixed32opaquealpha">DXVA2_Fixed32OpaqueAlpha</a> function.

### -field NoiseFilterLuma

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_filtervalues">DXVA2_FilterValues</a> structure that contains parameters for the luma noise filter.

### -field NoiseFilterChroma

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_filtervalues">DXVA2_FilterValues</a> structure that contains parameters for the chroma noise filter.

### -field DetailFilterLuma

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_filtervalues">DXVA2_FilterValues</a> structure that contains parameters for the luma detail filter.

### -field DetailFilterChroma

A <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_filtervalues">DXVA2_FilterValues</a> structure that contains parameters for the chroma detail filter.

### -field DestData

Contains additional flags. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DestData_RFF"></a><a id="dxva2_destdata_rff"></a><a id="DXVA2_DESTDATA_RFF"></a><dl>
<dt><b>DXVA2_DestData_RFF</b></dt>
</dl>
</td>
<td width="60%">
Repeat first field (RFF) bit.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DestData_TFF"></a><a id="dxva2_destdata_tff"></a><a id="DXVA2_DESTDATA_TFF"></a><dl>
<dt><b>DXVA2_DestData_TFF</b></dt>
</dl>
</td>
<td width="60%">
Top field first (TFF) bit.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DestData_RFF_TFF_Present"></a><a id="dxva2_destdata_rff_tff_present"></a><a id="DXVA2_DESTDATA_RFF_TFF_PRESENT"></a><dl>
<dt><b>DXVA2_DestData_RFF_TFF_Present</b></dt>
</dl>
</td>
<td width="60%">
If set, the RFF and TFF flags are used.
              

</td>
</tr>
</table>
 

Currently, these flags are ignored. They are intended for use with interlaced output, which is not supported at this time.

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>