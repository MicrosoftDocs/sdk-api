---
UID: NS:dxva2api._DXVA2_VideoProcessorCaps
title: DXVA2_VideoProcessorCaps (dxva2api.h)
description: Describes the capabilities of a DirectX Video Acceleration (DVXA) video processor mode.
helpviewer_keywords: ["DXVA2_DeinterlaceTech_BOBLineReplicate","DXVA2_DeinterlaceTech_BOBVerticalStretch","DXVA2_DeinterlaceTech_BOBVerticalStretch4Tap","DXVA2_DeinterlaceTech_EdgeFiltering","DXVA2_DeinterlaceTech_FieldAdaptive","DXVA2_DeinterlaceTech_InverseTelecine","DXVA2_DeinterlaceTech_MedianFiltering","DXVA2_DeinterlaceTech_MotionVectorSteered","DXVA2_DeinterlaceTech_PixelAdaptive","DXVA2_DeinterlaceTech_Unknown","DXVA2_DetailFilterTech_Edge","DXVA2_DetailFilterTech_Sharpening","DXVA2_DetailFilterTech_Unknown","DXVA2_DetailFilterTech_Unsupported","DXVA2_NoiseFilterTech_BlockNoise","DXVA2_NoiseFilterTech_Median","DXVA2_NoiseFilterTech_MosquitoNoise","DXVA2_NoiseFilterTech_Temporal","DXVA2_NoiseFilterTech_Unknown","DXVA2_NoiseFilterTech_Unsupported","DXVA2_VPDev_EmulatedDXVA1","DXVA2_VPDev_HardwareDevice","DXVA2_VPDev_SoftwareDevice","DXVA2_VideoProcess_AlphaBlend","DXVA2_VideoProcess_AlphaBlendExtended","DXVA2_VideoProcess_Constriction","DXVA2_VideoProcess_DetailFilter","DXVA2_VideoProcess_GammaCompensated","DXVA2_VideoProcess_LinearScaling","DXVA2_VideoProcess_MaintainsOriginalFieldData","DXVA2_VideoProcess_NoiseFilter","DXVA2_VideoProcess_PlanarAlpha","DXVA2_VideoProcess_StretchX","DXVA2_VideoProcess_StretchY","DXVA2_VideoProcess_SubRects","DXVA2_VideoProcess_SubStreams","DXVA2_VideoProcess_SubStreamsExtended","DXVA2_VideoProcess_YUV2RGB","DXVA2_VideoProcess_YUV2RGBExtended","DXVA2_VideoProcessorCaps","DXVA2_VideoProcessorCaps structure [Media Foundation]","cff01719-e653-4ea1-a177-9a6948b0da56","dxva2api/DXVA2_VideoProcessorCaps","mf.dxva2_videoprocessorcaps"]
old-location: mf\dxva2_videoprocessorcaps.htm
tech.root: mf
ms.assetid: cff01719-e653-4ea1-a177-9a6948b0da56
ms.date: 12/05/2018
ms.keywords: DXVA2_DeinterlaceTech_BOBLineReplicate, DXVA2_DeinterlaceTech_BOBVerticalStretch, DXVA2_DeinterlaceTech_BOBVerticalStretch4Tap, DXVA2_DeinterlaceTech_EdgeFiltering, DXVA2_DeinterlaceTech_FieldAdaptive, DXVA2_DeinterlaceTech_InverseTelecine, DXVA2_DeinterlaceTech_MedianFiltering, DXVA2_DeinterlaceTech_MotionVectorSteered, DXVA2_DeinterlaceTech_PixelAdaptive, DXVA2_DeinterlaceTech_Unknown, DXVA2_DetailFilterTech_Edge, DXVA2_DetailFilterTech_Sharpening, DXVA2_DetailFilterTech_Unknown, DXVA2_DetailFilterTech_Unsupported, DXVA2_NoiseFilterTech_BlockNoise, DXVA2_NoiseFilterTech_Median, DXVA2_NoiseFilterTech_MosquitoNoise, DXVA2_NoiseFilterTech_Temporal, DXVA2_NoiseFilterTech_Unknown, DXVA2_NoiseFilterTech_Unsupported, DXVA2_VPDev_EmulatedDXVA1, DXVA2_VPDev_HardwareDevice, DXVA2_VPDev_SoftwareDevice, DXVA2_VideoProcess_AlphaBlend, DXVA2_VideoProcess_AlphaBlendExtended, DXVA2_VideoProcess_Constriction, DXVA2_VideoProcess_DetailFilter, DXVA2_VideoProcess_GammaCompensated, DXVA2_VideoProcess_LinearScaling, DXVA2_VideoProcess_MaintainsOriginalFieldData, DXVA2_VideoProcess_NoiseFilter, DXVA2_VideoProcess_PlanarAlpha, DXVA2_VideoProcess_StretchX, DXVA2_VideoProcess_StretchY, DXVA2_VideoProcess_SubRects, DXVA2_VideoProcess_SubStreams, DXVA2_VideoProcess_SubStreamsExtended, DXVA2_VideoProcess_YUV2RGB, DXVA2_VideoProcess_YUV2RGBExtended, DXVA2_VideoProcessorCaps, DXVA2_VideoProcessorCaps structure [Media Foundation], cff01719-e653-4ea1-a177-9a6948b0da56, dxva2api/DXVA2_VideoProcessorCaps, mf.dxva2_videoprocessorcaps
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
req.typenames: DXVA2_VideoProcessorCaps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoProcessorCaps
 - dxva2api/_DXVA2_VideoProcessorCaps
 - DXVA2_VideoProcessorCaps
 - dxva2api/DXVA2_VideoProcessorCaps
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
 - DXVA2_VideoProcessorCaps
---

# DXVA2_VideoProcessorCaps structure


## -description

Describes the capabilities of a DirectX Video Acceleration (DVXA) video processor mode.

## -struct-fields

### -field DeviceCaps

Identifies the type of device. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VPDev_EmulatedDXVA1"></a><a id="dxva2_vpdev_emulateddxva1"></a><a id="DXVA2_VPDEV_EMULATEDDXVA1"></a><dl>
<dt><b>DXVA2_VPDev_EmulatedDXVA1</b></dt>
</dl>
</td>
<td width="60%">
DXVA 2.0 video processing is emulated by using DXVA 1.0. An emulated device may be missing significant processing capabilities and have lower image quality and performance.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VPDev_HardwareDevice"></a><a id="dxva2_vpdev_hardwaredevice"></a><a id="DXVA2_VPDEV_HARDWAREDEVICE"></a><dl>
<dt><b>DXVA2_VPDev_HardwareDevice</b></dt>
</dl>
</td>
<td width="60%">
Hardware device.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VPDev_SoftwareDevice"></a><a id="dxva2_vpdev_softwaredevice"></a><a id="DXVA2_VPDEV_SOFTWAREDEVICE"></a><dl>
<dt><b>DXVA2_VPDev_SoftwareDevice</b></dt>
</dl>
</td>
<td width="60%">
Software device.

</td>
</tr>
</table>

### -field InputPool

The Direct3D memory pool used by the device.

### -field NumForwardRefSamples

Number of forward reference samples the device needs to perform deinterlacing. For the bob, progressive scan, and software devices, the value is zero.

### -field NumBackwardRefSamples

Number of backward reference samples the device needs to perform deinterlacing. For the bob, progressive scan, and software devices, the value is zero.

### -field Reserved

Reserved. Must be zero.

### -field DeinterlaceTechnology

Identifies the deinterlacing technique used by the device. This value is a bitwise <b>OR</b> of one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_Unknown"></a><a id="dxva2_deinterlacetech_unknown"></a><a id="DXVA2_DEINTERLACETECH_UNKNOWN"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_Unknown</b></dt>
</dl>
</td>
<td width="60%">
The algorithm is unknown or proprietary.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_BOBLineReplicate"></a><a id="dxva2_deinterlacetech_boblinereplicate"></a><a id="DXVA2_DEINTERLACETECH_BOBLINEREPLICATE"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_BOBLineReplicate</b></dt>
</dl>
</td>
<td width="60%">
The algorithm creates missing lines by repeating the line either above or below the missing line. This algorithm produces a jagged image and is not recommended.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_BOBVerticalStretch"></a><a id="dxva2_deinterlacetech_bobverticalstretch"></a><a id="DXVA2_DEINTERLACETECH_BOBVERTICALSTRETCH"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_BOBVerticalStretch</b></dt>
</dl>
</td>
<td width="60%">
The algorithm creates missing lines by averaging two lines. Slight vertical adjustments are made so that the resulting image does not bob up and down.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_BOBVerticalStretch4Tap"></a><a id="dxva2_deinterlacetech_bobverticalstretch4tap"></a><a id="DXVA2_DEINTERLACETECH_BOBVERTICALSTRETCH4TAP"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_BOBVerticalStretch4Tap</b></dt>
</dl>
</td>
<td width="60%">
The algorithm creates missing lines by applying a [−1, 9, 9, −1]/16 filter across four lines. Slight vertical adjustments are made so that the resulting image does not bob up and down.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_MedianFiltering"></a><a id="dxva2_deinterlacetech_medianfiltering"></a><a id="DXVA2_DEINTERLACETECH_MEDIANFILTERING"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_MedianFiltering</b></dt>
</dl>
</td>
<td width="60%">
The algorithm uses median filtering to recreate the pixels in the missing lines.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_EdgeFiltering"></a><a id="dxva2_deinterlacetech_edgefiltering"></a><a id="DXVA2_DEINTERLACETECH_EDGEFILTERING"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_EdgeFiltering</b></dt>
</dl>
</td>
<td width="60%">
The algorithm uses an edge filter to create the missing lines. In this process, spatial directional filters are applied to determine the orientation of edges in the picture content. Missing pixels are created by filtering along (rather than across) the detected edges.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_FieldAdaptive"></a><a id="dxva2_deinterlacetech_fieldadaptive"></a><a id="DXVA2_DEINTERLACETECH_FIELDADAPTIVE"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_FieldAdaptive</b></dt>
</dl>
</td>
<td width="60%">
The algorithm uses spatial or temporal interpolation, switching between the two on a field-by-field basis, depending on the amount of motion.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_PixelAdaptive"></a><a id="dxva2_deinterlacetech_pixeladaptive"></a><a id="DXVA2_DEINTERLACETECH_PIXELADAPTIVE"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_PixelAdaptive</b></dt>
</dl>
</td>
<td width="60%">
The algorithm uses spatial or temporal interpolation, switching between the two on a pixel-by-pixel basis, depending on the amount of motion.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_MotionVectorSteered"></a><a id="dxva2_deinterlacetech_motionvectorsteered"></a><a id="DXVA2_DEINTERLACETECH_MOTIONVECTORSTEERED"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_MotionVectorSteered</b></dt>
</dl>
</td>
<td width="60%">
The algorithm identifies objects within a sequence of video fields. Before it recreates the missing pixels, it aligns the movement axes of the individual objects in the scene to make them parallel with the time axis.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeinterlaceTech_InverseTelecine"></a><a id="dxva2_deinterlacetech_inversetelecine"></a><a id="DXVA2_DEINTERLACETECH_INVERSETELECINE"></a><dl>
<dt><b>DXVA2_DeinterlaceTech_InverseTelecine</b></dt>
</dl>
</td>
<td width="60%">
The device can undo the 3:2 pulldown process used in telecine.

</td>
</tr>
</table>

### -field ProcAmpControlCaps

Specifies the available video processor (ProcAmp) operations. The value is a bitwise OR of <a href="/windows/desktop/medfound/procamp-settings">ProcAmp Settings</a> constants.

### -field VideoProcessorOperations

Specifies operations that the device can perform concurrently with the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt">IDirectXVideoProcessor::VideoProcessBlt</a> operation. The value is a bitwise <b>OR</b> of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_YUV2RGB"></a><a id="dxva2_videoprocess_yuv2rgb"></a><a id="DXVA2_VIDEOPROCESS_YUV2RGB"></a><dl>
<dt><b>DXVA2_VideoProcess_YUV2RGB</b></dt>
</dl>
</td>
<td width="60%">
The device can convert the video from YUV color space to RGB color space, with at least 8 bits of precision for each RGB component.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_StretchX"></a><a id="dxva2_videoprocess_stretchx"></a><a id="DXVA2_VIDEOPROCESS_STRETCHX"></a><dl>
<dt><b>DXVA2_VideoProcess_StretchX</b></dt>
</dl>
</td>
<td width="60%">
The device can stretch or shrink the video horizontally. If this capability is present, aspect ratio correction can be performed at the same time as deinterlacing.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_StretchY"></a><a id="dxva2_videoprocess_stretchy"></a><a id="DXVA2_VIDEOPROCESS_STRETCHY"></a><dl>
<dt><b>DXVA2_VideoProcess_StretchY</b></dt>
</dl>
</td>
<td width="60%">
The device can stretch or shrink the video vertically. If this capability is present, image resizing and aspect ratio correction can be performed at the same time.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_AlphaBlend"></a><a id="dxva2_videoprocess_alphablend"></a><a id="DXVA2_VIDEOPROCESS_ALPHABLEND"></a><dl>
<dt><b>DXVA2_VideoProcess_AlphaBlend</b></dt>
</dl>
</td>
<td width="60%">
The device can alpha blend the video.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_SubRects"></a><a id="dxva2_videoprocess_subrects"></a><a id="DXVA2_VIDEOPROCESS_SUBRECTS"></a><dl>
<dt><b>DXVA2_VideoProcess_SubRects</b></dt>
</dl>
</td>
<td width="60%">
The device can operate on a subrectangle of the video frame. If this capability is present, source images can be cropped before further processing occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_SubStreams"></a><a id="dxva2_videoprocess_substreams"></a><a id="DXVA2_VIDEOPROCESS_SUBSTREAMS"></a><dl>
<dt><b>DXVA2_VideoProcess_SubStreams</b></dt>
</dl>
</td>
<td width="60%">
The device can accept substreams in addition to the primary video stream, and can composite them.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_SubStreamsExtended"></a><a id="dxva2_videoprocess_substreamsextended"></a><a id="DXVA2_VIDEOPROCESS_SUBSTREAMSEXTENDED"></a><dl>
<dt><b>DXVA2_VideoProcess_SubStreamsExtended</b></dt>
</dl>
</td>
<td width="60%">
The device can perform color adjustments on the primary video stream and substreams, at the same time that it deinterlaces the video and composites the substreams. The destination color space is defined in the <b>DestFormat</b> member of the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams">DXVA2_VideoProcessBltParams</a> structure. The source color space for each stream is defined in the SampleFormat member of the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample">DXVA2_VideoSample</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_YUV2RGBExtended"></a><a id="dxva2_videoprocess_yuv2rgbextended"></a><a id="DXVA2_VIDEOPROCESS_YUV2RGBEXTENDED"></a><dl>
<dt><b>DXVA2_VideoProcess_YUV2RGBExtended</b></dt>
</dl>
</td>
<td width="60%">
The device can convert the video from YUV to RGB color space when it writes the deinterlaced and composited pixels to the destination surface.

An RGB destination surface could be an off-screen surface, texture, Direct3D render target, or combined texture/render target surface. An RGB destination surface must use at least 8 bits for each color channel.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_AlphaBlendExtended"></a><a id="dxva2_videoprocess_alphablendextended"></a><a id="DXVA2_VIDEOPROCESS_ALPHABLENDEXTENDED"></a><dl>
<dt><b>DXVA2_VideoProcess_AlphaBlendExtended</b></dt>
</dl>
</td>
<td width="60%">
The device can perform an alpha blend operation with the destination surface when it writes the deinterlaced and composited pixels to the destination surface.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_Constriction"></a><a id="dxva2_videoprocess_constriction"></a><a id="DXVA2_VIDEOPROCESS_CONSTRICTION"></a><dl>
<dt><b>DXVA2_VideoProcess_Constriction</b></dt>
</dl>
</td>
<td width="60%">
The device can downsample the output frame, as specified by the <b>ConstrictionSize</b> member of the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams">DXVA2_VideoProcessBltParams</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_NoiseFilter"></a><a id="dxva2_videoprocess_noisefilter"></a><a id="DXVA2_VIDEOPROCESS_NOISEFILTER"></a><dl>
<dt><b>DXVA2_VideoProcess_NoiseFilter</b></dt>
</dl>
</td>
<td width="60%">
The device can perform noise filtering.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_DetailFilter"></a><a id="dxva2_videoprocess_detailfilter"></a><a id="DXVA2_VIDEOPROCESS_DETAILFILTER"></a><dl>
<dt><b>DXVA2_VideoProcess_DetailFilter</b></dt>
</dl>
</td>
<td width="60%">
The device can perform detail filtering.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_PlanarAlpha"></a><a id="dxva2_videoprocess_planaralpha"></a><a id="DXVA2_VIDEOPROCESS_PLANARALPHA"></a><dl>
<dt><b>DXVA2_VideoProcess_PlanarAlpha</b></dt>
</dl>
</td>
<td width="60%">
The device can perform a constant alpha blend to the entire video stream when it composites the video stream and substreams.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_LinearScaling"></a><a id="dxva2_videoprocess_linearscaling"></a><a id="DXVA2_VIDEOPROCESS_LINEARSCALING"></a><dl>
<dt><b>DXVA2_VideoProcess_LinearScaling</b></dt>
</dl>
</td>
<td width="60%">
The device can perform accurate linear RGB scaling, rather than performing them in nonlinear gamma space.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_GammaCompensated"></a><a id="dxva2_videoprocess_gammacompensated"></a><a id="DXVA2_VIDEOPROCESS_GAMMACOMPENSATED"></a><dl>
<dt><b>DXVA2_VideoProcess_GammaCompensated</b></dt>
</dl>
</td>
<td width="60%">
The device can correct the image to compensate for artifacts introduced when performing scaling in nonlinear gamma space.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcess_MaintainsOriginalFieldData"></a><a id="dxva2_videoprocess_maintainsoriginalfielddata"></a><a id="DXVA2_VIDEOPROCESS_MAINTAINSORIGINALFIELDDATA"></a><dl>
<dt><b>DXVA2_VideoProcess_MaintainsOriginalFieldData</b></dt>
</dl>
</td>
<td width="60%">
The deinterlacing algorithm preserves the original field lines from the interlaced field picture, unless scaling is also applied.

For example, in deinterlacing algorithms such as bob and median filtering, the device copies the original field into every other scan line and then applies a filter to reconstruct the missing scan lines. As a result, the original field can be recovered by discarding the scan lines that were interpolated.

If the image is scaled vertically, however, the original field lines cannot be recovered. If the image is scaled horizontally (but not vertically), the resulting field lines will be equivalent to scaling the original field picture. (In other words, discarding the interpolated scan lines will yield the same result as stretching the original picture without deinterlacing.)

</td>
</tr>
</table>

### -field NoiseFilterTechnology

Specifies the supported noise filters. The value is a bitwise <b>OR</b> of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_Unsupported"></a><a id="dxva2_noisefiltertech_unsupported"></a><a id="DXVA2_NOISEFILTERTECH_UNSUPPORTED"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_Unsupported</b></dt>
</dl>
</td>
<td width="60%">
Noise filtering is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_Unknown"></a><a id="dxva2_noisefiltertech_unknown"></a><a id="DXVA2_NOISEFILTERTECH_UNKNOWN"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_Unknown</b></dt>
</dl>
</td>
<td width="60%">
Unknown or proprietary filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_Median"></a><a id="dxva2_noisefiltertech_median"></a><a id="DXVA2_NOISEFILTERTECH_MEDIAN"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_Median</b></dt>
</dl>
</td>
<td width="60%">
Median filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_Temporal"></a><a id="dxva2_noisefiltertech_temporal"></a><a id="DXVA2_NOISEFILTERTECH_TEMPORAL"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_Temporal</b></dt>
</dl>
</td>
<td width="60%">
Temporal filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_BlockNoise"></a><a id="dxva2_noisefiltertech_blocknoise"></a><a id="DXVA2_NOISEFILTERTECH_BLOCKNOISE"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_BlockNoise</b></dt>
</dl>
</td>
<td width="60%">
Block noise filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_NoiseFilterTech_MosquitoNoise"></a><a id="dxva2_noisefiltertech_mosquitonoise"></a><a id="DXVA2_NOISEFILTERTECH_MOSQUITONOISE"></a><dl>
<dt><b>DXVA2_NoiseFilterTech_MosquitoNoise</b></dt>
</dl>
</td>
<td width="60%">
Mosquito noise filter.

</td>
</tr>
</table>

### -field DetailFilterTechnology

Specifies the supported detail filters. The value is a bitwise <b>OR</b> of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DetailFilterTech_Unsupported"></a><a id="dxva2_detailfiltertech_unsupported"></a><a id="DXVA2_DETAILFILTERTECH_UNSUPPORTED"></a><dl>
<dt><b>DXVA2_DetailFilterTech_Unsupported</b></dt>
</dl>
</td>
<td width="60%">
Detail filtering is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DetailFilterTech_Unknown"></a><a id="dxva2_detailfiltertech_unknown"></a><a id="DXVA2_DETAILFILTERTECH_UNKNOWN"></a><dl>
<dt><b>DXVA2_DetailFilterTech_Unknown</b></dt>
</dl>
</td>
<td width="60%">
Unknown or proprietary filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DetailFilterTech_Edge"></a><a id="dxva2_detailfiltertech_edge"></a><a id="DXVA2_DETAILFILTERTECH_EDGE"></a><dl>
<dt><b>DXVA2_DetailFilterTech_Edge</b></dt>
</dl>
</td>
<td width="60%">
Edge filter.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DetailFilterTech_Sharpening"></a><a id="dxva2_detailfiltertech_sharpening"></a><a id="DXVA2_DETAILFILTERTECH_SHARPENING"></a><dl>
<dt><b>DXVA2_DetailFilterTech_Sharpening</b></dt>
</dl>
</td>
<td width="60%">
Sharpen filter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getvideoprocessorcaps">IDirectXVideoProcessor::GetVideoProcessorCaps</a>



<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps">IDirectXVideoProcessorService::GetVideoProcessorCaps</a>



<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>