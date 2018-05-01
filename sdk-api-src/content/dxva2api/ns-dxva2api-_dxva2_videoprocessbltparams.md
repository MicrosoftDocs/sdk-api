---
UID: NS:dxva2api._DXVA2_VideoProcessBltParams
title: "_DXVA2_VideoProcessBltParams"
author: windows-driver-content
description: Contains parameters for the IDirectXVideoProcessor::VideoProcessBlt method.
old-location: mf\dxva2_videoprocessbltparams.htm
old-project: medfound
ms.assetid: 6929fa8b-3cab-4d4e-ab2a-a3059b00905f
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 6929fa8b-3cab-4d4e-ab2a-a3059b00905f, DXVA2_DestData_RFF, DXVA2_DestData_RFF_TFF_Present, DXVA2_DestData_TFF, DXVA2_VideoProcessBltParams, DXVA2_VideoProcessBltParams structure [Media Foundation], _DXVA2_VideoProcessBltParams, dxva2api/DXVA2_VideoProcessBltParams, mf.dxva2_videoprocessbltparams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DXVA2_VideoProcessBltParams
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva2api.h
api_name:
-	DXVA2_VideoProcessBltParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA2_VideoProcessBltParams structure


## -description



Contains parameters for the <a href="https://msdn.microsoft.com/4a199ad3-621e-4594-a9f8-ad6cfd560cec">IDirectXVideoProcessor::VideoProcessBlt</a> method.




## -struct-fields




### -field TargetFrame

Presentation time for the target frame, in 100-nanosecond units. If the video is interlaced, this value must be either the start time for the frame or the midpoint for the frame. If the video is progressive, this value must be the start time.


### -field TargetRect


            Specifies the target rectangle, which is the rectangle within the destination surface where the output video frame is drawn.
          

The target rectangle cannot be larger than the destination surface.


### -field ConstrictionSize


            Size to which the output video should be downsampled. 
          If this feature is supported, the driver sets the <b>DXVA2_VideoProcess_Constriction</b> flag in the <a href="https://msdn.microsoft.com/cff01719-e653-4ea1-a177-9a6948b0da56">DXVA2_VideoProcessorCaps</a> structure.

The downsampling size cannot be less than zero, or larger than the size of the target rectangle (<b>TargetRect</b>).  


### -field StreamingFlags


            Reserved. Set to zero.
          


### -field BackgroundColor

A <a href="https://msdn.microsoft.com/3e25182a-fd5d-437c-9441-44094a3450cb">DXVA2_AYUVSample16</a> structure that specifies the background color for the destination rectangle. The background color is used wherever no video image appears, but only within the <b>TargetRect</b> rectangle. The color is specified as an AYUV color value with 16 bits per channel. 

The alpha channel (<b>Alpha</b>) must be opaque (0xFFFF). The DXVA driver should ignore the value of the alpha channel. 

The color space for the background color is given by the <b>DestFormat</b> member. Note that the background color is always specified as a YUV color, even if the destination surface is RGB.


### -field DestFormat

A <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure that contains extended color information for the destination rectangle. For video playback, the recommended value for the nominal range is DXVA2_NominalRange_Unknown. For more information, see <a href="https://msdn.microsoft.com/ebc146e4-517f-4413-93dc-66cf4b3a04c3">DXVA2_NominalRange</a> enumeration.


### -field ProcAmpValues

A <a href="https://msdn.microsoft.com/c84acd34-e922-46bb-9913-0f94c7c47155">DXVA2_ProcAmpValues</a> structure that specifies color adjustment (ProcAmp) settings. These values must fall within the ranges returned by the <a href="https://msdn.microsoft.com/e15c8425-7a0b-4d03-b2da-467c800c57c2">IDirectXVideoProcessor::GetProcAmpRange</a> method.


### -field Alpha


            Alpha value that is applied to the composited image when it is copied to the destination surface. The alpha value is fixed-point value, specified as a <a href="https://msdn.microsoft.com/5f8f4515-1cf4-4060-813b-c746649c5c40">DXVA2_Fixed32</a> structure. To specify 100% opacity, use the <a href="https://msdn.microsoft.com/de2f8aa8-0e06-4f47-9d69-dfff07bc4c0f">DXVA2_Fixed32OpaqueAlpha</a> function.
          


### -field NoiseFilterLuma

A <a href="https://msdn.microsoft.com/48dc1631-f96c-4515-aac2-225b3427f9ad">DXVA2_FilterValues</a> structure that contains parameters for the luma noise filter.


### -field NoiseFilterChroma

A <a href="https://msdn.microsoft.com/48dc1631-f96c-4515-aac2-225b3427f9ad">DXVA2_FilterValues</a> structure that contains parameters for the chroma noise filter.


### -field DetailFilterLuma

A <a href="https://msdn.microsoft.com/48dc1631-f96c-4515-aac2-225b3427f9ad">DXVA2_FilterValues</a> structure that contains parameters for the luma detail filter.


### -field DetailFilterChroma

A <a href="https://msdn.microsoft.com/48dc1631-f96c-4515-aac2-225b3427f9ad">DXVA2_FilterValues</a> structure that contains parameters for the chroma detail filter.


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




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

