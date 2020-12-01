---
UID: NS:mfobjects._MFVideoInfo
title: MFVideoInfo (mfobjects.h)
description: Contains video format information that applies to both compressed and uncompressed formats.This structure is used in the MFVIDEOFORMAT structure.
helpviewer_keywords: ["746fd84f-58f8-42ab-bcf7-8fd18dcd02af","MFVideoInfo","MFVideoInfo structure [Media Foundation]","mf.mfvideoinfo","mfobjects/MFVideoInfo"]
old-location: mf\mfvideoinfo.htm
tech.root: mf
ms.assetid: 746fd84f-58f8-42ab-bcf7-8fd18dcd02af
ms.date: 12/05/2018
ms.keywords: 746fd84f-58f8-42ab-bcf7-8fd18dcd02af, MFVideoInfo, MFVideoInfo structure [Media Foundation], mf.mfvideoinfo, mfobjects/MFVideoInfo
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
targetos: Windows
req.typenames: MFVideoInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoInfo
 - mfobjects/_MFVideoInfo
 - MFVideoInfo
 - mfobjects/MFVideoInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFVideoInfo
---

# MFVideoInfo structure


## -description

Contains video format information that applies to both compressed and uncompressed formats.

This structure is used in the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -struct-fields

### -field dwWidth

Width of the decoded image, in pixels.

### -field dwHeight

Height of the decoded image, in pixels.

### -field PixelAspectRatio

Pixel aspect ratio, specified as an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfratio">MFRatio</a> structure.

### -field SourceChromaSubsampling

Chroma sub-sampling of the original image, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling">MFVideoChromaSubsampling</a> enumeration.

### -field InterlaceMode

Image interlacing, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode">MFVideoInterlaceMode</a> enumeration.

### -field TransferFunction

R'G'B' gamma curve function, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction">MFVideoTransferFunction</a> enumeration.

### -field ColorPrimaries

Color primaries of the video source, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries">MFVideoPrimaries</a> enumeration. This value provides the conversion from R'G'B' to linear RGB.

### -field TransferMatrix

Conversion matrix from Y'Cb'Cr' to R'G'B, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix">MFVideoTransferMatrix</a> enumeration.

### -field SourceLighting

Intended viewing conditions, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideolighting">MFVideoLighting</a> enumeration.

### -field FramesPerSecond

Frames per second, specified as an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfratio">MFRatio</a> structure. If the frame rate is unknown or variable, the numerator and denominator should both be set to zero. It is invalid for only one member of the <b>MFRatio</b> structure to be zero.

### -field NominalRange

Range of valid RGB values, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange">MFNominalRange</a> enumeration. The value indicates whether color values contain headroom and toeroom.

### -field GeometricAperture

Geometric aperture, specified as an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea">MFVideoArea</a> structure. For more information, see <a href="/windows/desktop/medfound/mf-mt-geometric-aperture-attribute">MF_MT_GEOMETRIC_APERTURE</a>.

### -field MinimumDisplayAperture

The display aperture, specified as an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea">MFVideoArea</a> structure. The display aperture is the region of the video image that is intended to be shown. Any data outside of this area is the overscan region. For more information, see <a href="/windows/desktop/medfound/mf-mt-minimum-display-aperture-attribute">MF_MT_MINIMUM_DISPLAY_APERTURE</a>.

### -field PanScanAperture

Pan-scan rectangle, specified as an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea">MFVideoArea</a> structure. The pan-scan rectangle defines a region of the image that is displayed in pan-and-scan mode. It can be used when wide-screen content is shown on a 4 x 3 display. The value is valid only when the <b>VideoFlags</b> member contains the MFVideoFlag_PanScanEnabled flag.

### -field VideoFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoflags">MFVideoFlags</a> enumeration.

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
<a href="/windows/desktop/medfound/mf-mt-frame-size-attribute">MF_MT_FRAME_SIZE</a>
</td>
</tr>
<tr>
<td><b>PixelAspectRatio</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-pixel-aspect-ratio-attribute">MF_MT_PIXEL_ASPECT_RATIO</a>
</td>
</tr>
<tr>
<td><b>SourceChromaSubsampling</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-video-chroma-siting-attribute">MF_MT_VIDEO_CHROMA_SITING</a>
</td>
</tr>
<tr>
<td><b>InterlaceMode</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-interlace-mode-attribute">MF_MT_INTERLACE_MODE</a>
</td>
</tr>
<tr>
<td><b>TransferFunction</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-transfer-function-attribute">MF_MT_TRANSFER_FUNCTION</a>
</td>
</tr>
<tr>
<td><b>ColorPrimaries</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-video-primaries-attribute">MF_MT_VIDEO_PRIMARIES</a>
</td>
</tr>
<tr>
<td><b>TransferMatrix</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-yuv-matrix-attribute">MF_MT_YUV_MATRIX</a>
</td>
</tr>
<tr>
<td><b>SourceLighting</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-video-lighting-attribute">MF_MT_VIDEO_LIGHTING</a>
</td>
</tr>
<tr>
<td><b>FramesPerSecond</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-frame-rate-attribute">MF_MT_FRAME_RATE</a>
</td>
</tr>
<tr>
<td><b>NominalRange</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-video-nominal-range-attribute">MF_MT_VIDEO_NOMINAL_RANGE</a>
</td>
</tr>
<tr>
<td><b>GeometricAperture</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-geometric-aperture-attribute">MF_MT_GEOMETRIC_APERTURE</a>
</td>
</tr>
<tr>
<td><b>MinimumDisplayAperture</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-minimum-display-aperture-attribute">MF_MT_MINIMUM_DISPLAY_APERTURE</a>
</td>
</tr>
<tr>
<td><b>PanScanAperture</b></td>
<td>
<a href="/windows/desktop/medfound/mf-mt-pan-scan-aperture-attribute">MF_MT_PAN_SCAN_APERTURE</a>
</td>
</tr>
<tr>
<td><b>VideoFlags</b></td>
<td>See <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoflags">MFVideoFlags</a>.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>