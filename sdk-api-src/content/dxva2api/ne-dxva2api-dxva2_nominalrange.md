---
UID: NE:dxva2api._DXVA2_NominalRange
title: DXVA2_NominalRange (dxva2api.h)
description: Describes how to map color data to a normalized [0...1] range.
helpviewer_keywords: ["DXVA2_NominalRange","DXVA2_NominalRange enumeration [Media Foundation]","DXVA2_NominalRangeMask","DXVA2_NominalRange_0_255","DXVA2_NominalRange_16_235","DXVA2_NominalRange_48_208","DXVA2_NominalRange_Normal","DXVA2_NominalRange_Unknown","DXVA2_NominalRange_Wide","dxva2api/DXVA2_NominalRange","dxva2api/DXVA2_NominalRangeMask","dxva2api/DXVA2_NominalRange_0_255","dxva2api/DXVA2_NominalRange_16_235","dxva2api/DXVA2_NominalRange_48_208","dxva2api/DXVA2_NominalRange_Normal","dxva2api/DXVA2_NominalRange_Unknown","dxva2api/DXVA2_NominalRange_Wide","ebc146e4-517f-4413-93dc-66cf4b3a04c3","mf.dxva2_nominalrange"]
old-location: mf\dxva2_nominalrange.htm
tech.root: mf
ms.assetid: ebc146e4-517f-4413-93dc-66cf4b3a04c3
ms.date: 12/05/2018
ms.keywords: DXVA2_NominalRange, DXVA2_NominalRange enumeration [Media Foundation], DXVA2_NominalRangeMask, DXVA2_NominalRange_0_255, DXVA2_NominalRange_16_235, DXVA2_NominalRange_48_208, DXVA2_NominalRange_Normal, DXVA2_NominalRange_Unknown, DXVA2_NominalRange_Wide, dxva2api/DXVA2_NominalRange, dxva2api/DXVA2_NominalRangeMask, dxva2api/DXVA2_NominalRange_0_255, dxva2api/DXVA2_NominalRange_16_235, dxva2api/DXVA2_NominalRange_48_208, dxva2api/DXVA2_NominalRange_Normal, dxva2api/DXVA2_NominalRange_Unknown, dxva2api/DXVA2_NominalRange_Wide, ebc146e4-517f-4413-93dc-66cf4b3a04c3, mf.dxva2_nominalrange
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
req.typenames: DXVA2_NominalRange
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_NominalRange
 - dxva2api/_DXVA2_NominalRange
 - DXVA2_NominalRange
 - dxva2api/DXVA2_NominalRange
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
 - DXVA2_NominalRange
---

# DXVA2_NominalRange enumeration


## -description

Describes how to map color data to a normalized [0...1] range. 

These flags are used in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure. They indicate whether the range of color values includes headroom (values above 100% white) and toeroom (values below reference black).

## -enum-fields

### -field DXVA2_NominalRangeMask:0x7

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_NominalRange_Unknown:0

Unknown or unspecified nominal range.

If this value is used in the <b>DestFormat</b> member of the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams">DXVA2_VideoProcessBltParams</a> structure, the driver will determine the optimal nominal range based on the destination color space. For example, the destination surface is usually sRGB, which has a nominal range of 0-255 per channel. However, a driver might use a technique such as automatic gain control to maximize the dynamic range while preserving values above reference white.

### -field DXVA2_NominalRange_Normal:1

Equivalent to DXVA2_NominalRange_0_255.

### -field DXVA2_NominalRange_Wide:2

Equivalent to DXVA2_NominalRange_16_235.

### -field DXVA2_NominalRange_0_255:1

The normalized range [0...1] maps to [0...255] for 8-bit samples or [0...1023] for 10-bit samples.

### -field DXVA2_NominalRange_16_235:2

The normalized range [0...1] maps to [16...235] for 8-bit samples or [64...940] for 10-bit samples.

### -field DXVA2_NominalRange_48_208:3

The normalized range [0..1] maps to [48...208] for 8-bit samples or [192...832] for 10-bit samples.

## -remarks

For YUV colors, these flags specify how to convert between Y'CbCr and Y'PbPr. The Y'PbPr color space has a range of [0..1] for Y' (luma) and [-0.5...0.5] for Pb/Pr (chroma).

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>DXVA2_NominalRange_0_255</td>
<td>Should not be used for YUV data.</td>
</tr>
<tr>
<td>DXVA2_NominalRange_16_235</td>
<td>
For 8-bit Y'CbCr components:

<ul>
<li>
Y' range of [0...1] maps to [16..235] for 8-bit Y' values.

</li>
<li>
Pb/Pr ranges of [-0.5...0.5] map to [16...240] for 8-bit Cb/Cr values.

</li>
</ul>
For samples with <i>n</i> bits of precision, the general equations are:

<ul>
<li>
Y' = (Y' * 219 + 16) * 2 ^ (n-8)
                  

</li>
<li>
Cb = (Pb * 224 + 128) * 2 ^ (n-8)
                  

</li>
<li>
Cr = (Pr * 224 + 128) * 2 ^ (n-8)
                  

</li>
</ul>
The inverse equations to convert from Y'CbCr to Y'PbPr are:

<ul>
<li>
Y' = (Y' / 2 ^ (n-8) - 16) / 219
                  

</li>
<li>
Pb = (Cb / 2 ^ (n-8) - 128) / 224
                  

</li>
<li>
Pr = (Cr / 2 ^ (n-8) - 128) / 224
                  

</li>
</ul>
</td>
</tr>
<tr>
<td>DXVA2_NominalRange_48_208</td>
<td>For 8-bit Y'CbCr values, Y' range of [0..1] maps to [48...208].</td>
</tr>
</table>
 

For RGB colors, the flags differentiate various RGB spaces.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>DXVA2_NominalRange_0_255</td>
<td>sRGB</td>
</tr>
<tr>
<td>DXVA2_NominalRange_16_235</td>
<td>Studio RGB; ITU-R BT.709</td>
</tr>
<tr>
<td>DXVA2_NominalRange_48_208</td>
<td>ITU-R BT.1361 RGB</td>
</tr>
</table>
 

Video data might contain values above or below the nominal range.

<div class="alert"><b>Note</b>  The values named  DXVA2_NominalRange_Normal and DXVA2_NominalRange_Wide are a potential source of confusion. <i>Wide</i> refers to the possible range of <i>analog</i> values that can be represented, by mapping the nominal range [0...1] into a narrower range of <i>digital</i> values. Because the meaning of <i>wide</i> in this context is ambiguous, the equivalent values named DXVA2_NominalRange_0_255 and DXVA2_NominalRange_16_235 are preferred. These names explicitly convey the meaning of the enumeration, and are less likely to be misinterpreted.</div>
<div> </div>
This enumeration is equivalent to the <b>DXVA_NominalRange</b> enumeration used in DXVA 1.0, although it defines additional values.

If you are using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface to describe the video format, the nominal range is specified in the <a href="/windows/desktop/medfound/mf-mt-video-nominal-range-attribute">MF_MT_VIDEO_NOMINAL_RANGE</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
