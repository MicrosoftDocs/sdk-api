---
UID: NS:mfobjects._MFVideoInfo
title: MFVideoInfo (mfobjects.h)
author: windows-sdk-content
description: Contains video format information that applies to both compressed and uncompressed formats.This structure is used in the MFVIDEOFORMAT structure.
old-location: mf\mfvideoinfo.htm
tech.root: medfound
ms.assetid: 746fd84f-58f8-42ab-bcf7-8fd18dcd02af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 746fd84f-58f8-42ab-bcf7-8fd18dcd02af, MFVideoInfo, MFVideoInfo structure [Media Foundation], mf.mfvideoinfo, mfobjects/MFVideoInfo
ms.topic: struct
req.header: mfobjects.h
req.include-header: Mfidl.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFVideoInfo
product: Windows
targetos: Windows
req.typenames: MFVideoInfo
req.redist: 
---

# MFVideoInfo structure


## -description



Contains video format information that applies to both compressed and uncompressed formats.

This structure is used in the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.




## -struct-fields




### -field dwWidth

Width of the decoded image, in pixels.
          


### -field dwHeight

Height of the decoded image, in pixels.
          


### -field PixelAspectRatio

Pixel aspect ratio, specified as an <a href="https://msdn.microsoft.com/315d31d6-bf68-4495-9bae-1f624f497c1a">MFRatio</a> structure.
          


### -field SourceChromaSubsampling

Chroma sub-sampling of the original image, specified as a member of the <a href="https://msdn.microsoft.com/778d0456-f98e-44ac-afb7-9ce01da06741">MFVideoChromaSubsampling</a> enumeration.
          


### -field InterlaceMode

Image interlacing, specified as a member of the <a href="https://msdn.microsoft.com/10a3d7b1-74ed-46cd-b10e-59a8f01726d5">MFVideoInterlaceMode</a> enumeration.
          


### -field TransferFunction

R'G'B' gamma curve function, specified as a member of the <a href="https://msdn.microsoft.com/f9aff1d5-e9f7-48fd-9c86-8dc597d37dfa">MFVideoTransferFunction</a> enumeration.
          


### -field ColorPrimaries

Color primaries of the video source, specified as a member of the <a href="https://msdn.microsoft.com/a1d6a60c-823c-46c3-a751-18e55fbc52a1">MFVideoPrimaries</a> enumeration. This value provides the conversion from R'G'B' to linear RGB.
          


### -field TransferMatrix

Conversion matrix from Y'Cb'Cr' to R'G'B, specified as a member of the <a href="https://msdn.microsoft.com/08a05ee8-b053-4480-b7f9-6d96e541ccd9">MFVideoTransferMatrix</a> enumeration.
          


### -field SourceLighting

Intended viewing conditions, specified as a member of the <a href="https://msdn.microsoft.com/2eeca357-b7e2-40b1-b19f-2e12a833c1ca">MFVideoLighting</a> enumeration.
          


### -field FramesPerSecond

Frames per second, specified as an <a href="https://msdn.microsoft.com/315d31d6-bf68-4495-9bae-1f624f497c1a">MFRatio</a> structure. If the frame rate is unknown or variable, the numerator and denominator should both be set to zero. It is invalid for only one member of the <b>MFRatio</b> structure to be zero.
          


### -field NominalRange

Range of valid RGB values, specified as a member of the <a href="https://msdn.microsoft.com/fe7547f8-84cd-461a-8d33-dbc0b90add37">MFNominalRange</a> enumeration. The value indicates whether color values contain headroom and toeroom.
          


### -field GeometricAperture

Geometric aperture, specified as an <a href="https://msdn.microsoft.com/d22b8b9c-399b-4fce-a173-833005b5bf03">MFVideoArea</a> structure. For more information, see <a href="https://msdn.microsoft.com/a2489ba1-f322-4b63-a479-0d9879c30a8c">MF_MT_GEOMETRIC_APERTURE</a>.
          


### -field MinimumDisplayAperture

The display aperture, specified as an <a href="https://msdn.microsoft.com/d22b8b9c-399b-4fce-a173-833005b5bf03">MFVideoArea</a> structure. The display aperture is the region of the video image that is intended to be shown. Any data outside of this area is the overscan region. For more information, see <a href="https://msdn.microsoft.com/86a7509b-c690-49c2-bbe4-8b02d64c307c">MF_MT_MINIMUM_DISPLAY_APERTURE</a>.
          


### -field PanScanAperture

Pan-scan rectangle, specified as an <a href="https://msdn.microsoft.com/d22b8b9c-399b-4fce-a173-833005b5bf03">MFVideoArea</a> structure. The pan-scan rectangle defines a region of the image that is displayed in pan-and-scan mode. It can be used when wide-screen content is shown on a 4 x 3 display. The value is valid only when the <b>VideoFlags</b> member contains the MFVideoFlag_PanScanEnabled flag.
          


### -field VideoFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/2530bf1d-05b1-4c16-b00b-117c0dadb301">MFVideoFlags</a> enumeration.
          


## -remarks



Developers are encouraged to use media type attributes instead of using the <b>MFVideoInfo</b> structure. The following table lists the attributes that correspond to the members of this structure.

<table>
<tr>
<th>Structure Member</th>
<th>Media Type Attribute</th>
</tr>
<tr>
<td><b>dwWidth</b>, <b>dwHeight</b></td>
<td>
<a href="https://msdn.microsoft.com/9f10a972-406f-47ef-b71c-86ed771c9a9a">MF_MT_FRAME_SIZE</a>
</td>
</tr>
<tr>
<td><b>PixelAspectRatio</b></td>
<td>
<a href="https://msdn.microsoft.com/e82cdd22-7d3f-4858-befd-43fa6f9f915e">MF_MT_PIXEL_ASPECT_RATIO</a>
</td>
</tr>
<tr>
<td><b>SourceChromaSubsampling</b></td>
<td>
<a href="https://msdn.microsoft.com/0c930348-8669-42cc-9d74-df9ef475bdc8">MF_MT_VIDEO_CHROMA_SITING</a>
</td>
</tr>
<tr>
<td><b>InterlaceMode</b></td>
<td>
<a href="https://msdn.microsoft.com/19aa0147-ac49-4a2e-ac75-e967fec9ca68">MF_MT_INTERLACE_MODE</a>
</td>
</tr>
<tr>
<td><b>TransferFunction</b></td>
<td>
<a href="https://msdn.microsoft.com/c64c2135-f588-4d7a-9ca8-ae4f7b290572">MF_MT_TRANSFER_FUNCTION</a>
</td>
</tr>
<tr>
<td><b>ColorPrimaries</b></td>
<td>
<a href="https://msdn.microsoft.com/56f31c1a-b610-4da0-9df4-76e15add672c">MF_MT_VIDEO_PRIMARIES</a>
</td>
</tr>
<tr>
<td><b>TransferMatrix</b></td>
<td>
<a href="https://msdn.microsoft.com/b268d16d-b4cc-4026-9ba7-805cc5409b95">MF_MT_YUV_MATRIX</a>
</td>
</tr>
<tr>
<td><b>SourceLighting</b></td>
<td>
<a href="https://msdn.microsoft.com/697590e3-898e-4ac9-8390-7b0994b6e571">MF_MT_VIDEO_LIGHTING</a>
</td>
</tr>
<tr>
<td><b>FramesPerSecond</b></td>
<td>
<a href="https://msdn.microsoft.com/8336559c-06f1-478e-b921-e9eae7425230">MF_MT_FRAME_RATE</a>
</td>
</tr>
<tr>
<td><b>NominalRange</b></td>
<td>
<a href="https://msdn.microsoft.com/7b2b809e-aae4-401c-816a-626fb88f5f87">MF_MT_VIDEO_NOMINAL_RANGE</a>
</td>
</tr>
<tr>
<td><b>GeometricAperture</b></td>
<td>
<a href="https://msdn.microsoft.com/a2489ba1-f322-4b63-a479-0d9879c30a8c">MF_MT_GEOMETRIC_APERTURE</a>
</td>
</tr>
<tr>
<td><b>MinimumDisplayAperture</b></td>
<td>
<a href="https://msdn.microsoft.com/86a7509b-c690-49c2-bbe4-8b02d64c307c">MF_MT_MINIMUM_DISPLAY_APERTURE</a>
</td>
</tr>
<tr>
<td><b>PanScanAperture</b></td>
<td>
<a href="https://msdn.microsoft.com/faa577fd-6572-46b9-9c6c-f91c47832cb5">MF_MT_PAN_SCAN_APERTURE</a>
</td>
</tr>
<tr>
<td><b>VideoFlags</b></td>
<td>See <a href="https://msdn.microsoft.com/2530bf1d-05b1-4c16-b00b-117c0dadb301">MFVideoFlags</a>.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

