---
UID: NE:dxva2api._DXVA2_VideoPrimaries
title: DXVA2_VideoPrimaries (dxva2api.h)
description: Specifies the color primaries of a video source.
helpviewer_keywords: ["4534a198-cf6c-4689-9fe4-0e5cdc7ce26a","DXVA2_VideoPrimaries","DXVA2_VideoPrimaries enumeration [Media Foundation]","DXVA2_VideoPrimariesMask","DXVA2_VideoPrimaries_BT470_2_SysBG","DXVA2_VideoPrimaries_BT470_2_SysM","DXVA2_VideoPrimaries_BT709","DXVA2_VideoPrimaries_EBU3213","DXVA2_VideoPrimaries_SMPTE170M","DXVA2_VideoPrimaries_SMPTE240M","DXVA2_VideoPrimaries_SMPTE_C","DXVA2_VideoPrimaries_Unknown","DXVA2_VideoPrimaries_reserved","dxva2api/DXVA2_VideoPrimaries","dxva2api/DXVA2_VideoPrimariesMask","dxva2api/DXVA2_VideoPrimaries_BT470_2_SysBG","dxva2api/DXVA2_VideoPrimaries_BT470_2_SysM","dxva2api/DXVA2_VideoPrimaries_BT709","dxva2api/DXVA2_VideoPrimaries_EBU3213","dxva2api/DXVA2_VideoPrimaries_SMPTE170M","dxva2api/DXVA2_VideoPrimaries_SMPTE240M","dxva2api/DXVA2_VideoPrimaries_SMPTE_C","dxva2api/DXVA2_VideoPrimaries_Unknown","dxva2api/DXVA2_VideoPrimaries_reserved","mf.dxva2_videoprimaries"]
old-location: mf\dxva2_videoprimaries.htm
tech.root: mf
ms.assetid: 4534a198-cf6c-4689-9fe4-0e5cdc7ce26a
ms.date: 12/05/2018
ms.keywords: 4534a198-cf6c-4689-9fe4-0e5cdc7ce26a, DXVA2_VideoPrimaries, DXVA2_VideoPrimaries enumeration [Media Foundation], DXVA2_VideoPrimariesMask, DXVA2_VideoPrimaries_BT470_2_SysBG, DXVA2_VideoPrimaries_BT470_2_SysM, DXVA2_VideoPrimaries_BT709, DXVA2_VideoPrimaries_EBU3213, DXVA2_VideoPrimaries_SMPTE170M, DXVA2_VideoPrimaries_SMPTE240M, DXVA2_VideoPrimaries_SMPTE_C, DXVA2_VideoPrimaries_Unknown, DXVA2_VideoPrimaries_reserved, dxva2api/DXVA2_VideoPrimaries, dxva2api/DXVA2_VideoPrimariesMask, dxva2api/DXVA2_VideoPrimaries_BT470_2_SysBG, dxva2api/DXVA2_VideoPrimaries_BT470_2_SysM, dxva2api/DXVA2_VideoPrimaries_BT709, dxva2api/DXVA2_VideoPrimaries_EBU3213, dxva2api/DXVA2_VideoPrimaries_SMPTE170M, dxva2api/DXVA2_VideoPrimaries_SMPTE240M, dxva2api/DXVA2_VideoPrimaries_SMPTE_C, dxva2api/DXVA2_VideoPrimaries_Unknown, dxva2api/DXVA2_VideoPrimaries_reserved, mf.dxva2_videoprimaries
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
req.typenames: DXVA2_VideoPrimaries
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoPrimaries
 - dxva2api/_DXVA2_VideoPrimaries
 - DXVA2_VideoPrimaries
 - dxva2api/DXVA2_VideoPrimaries
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
 - DXVA2_VideoPrimaries
---

# DXVA2_VideoPrimaries enumeration


## -description

Specifies the color primaries of a video source. These flags are used in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.

## -enum-fields

### -field DXVA2_VideoPrimariesMask:0x1f

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_VideoPrimaries_Unknown:0

Unknown. Treat as <b>DXVA2_VideoPrimaries_BT709</b>.

### -field DXVA2_VideoPrimaries_reserved:1

Reserved. Do not use.

### -field DXVA2_VideoPrimaries_BT709:2

ITU-R BT.709. Also used for sRGB and scRGB.

### -field DXVA2_VideoPrimaries_BT470_2_SysM:3

ITU-R BT.470-4 System M (NTSC).

### -field DXVA2_VideoPrimaries_BT470_2_SysBG:4

ITU-R BT.470-4 System B,G (PAL).

### -field DXVA2_VideoPrimaries_SMPTE170M:5

SMPTE 170M.

### -field DXVA2_VideoPrimaries_SMPTE240M:6

SMPTE 240M.

### -field DXVA2_VideoPrimaries_EBU3213:7

EBU Tech. 3213.

### -field DXVA2_VideoPrimaries_SMPTE_C:8

SMPTE C (SMPTE RP 145).

## -remarks

Color primaries define how to convert RGB colors into the CIE XYZ color space, and can be used to translate colors between different RGB color spaces. An RGB color space is defined by the chromaticity coordinates (x,y) of the RGB primaries plus the white point, as listed in the following table.

<table>
<tr>
<th>Color space</th>
<th>(Rx, Ry)</th>
<th>(Gx, Gy)</th>
<th>(Bx, By)</th>
<th>White point (Wx, Wy)</th>
</tr>
<tr>
<td>BT.709</td>
<td>(0.64, 0.33)</td>
<td>(0.30, 0.60)</td>
<td>(0.15, 0.06)</td>
<td>D65
              (0.3127, 0.3290)
            </td>
</tr>
<tr>
<td>BT.470-2 System B,G;
              EBU 3213
            </td>
<td>(0.64, 0.33)</td>
<td>(0.29, 0.60)</td>
<td>(0.15, 0.06)</td>
<td>D65
              (0.3127, 0.3290)
            </td>
</tr>
<tr>
<td>BT.470-4 System M</td>
<td>(0.67, 0.33)</td>
<td>(0.21, 0.71)</td>
<td>(0.14, 0.08)</td>
<td>CIE III.C
              (0.310, 0.316)
            </td>
</tr>
<tr>
<td>SMPTE 170M; SMPTE 240M;
              SMPTE C
            </td>
<td>(0.63, 0.34)</td>
<td>(0.31, 0.595)</td>
<td>(0.155, 0.07)</td>
<td>D65
              (0.3127, 0.3291)
            </td>
</tr>
</table>
 

The z coordinates can be derived from x and y as follows: z = 1 - x - y. To convert between RGB colors to CIE XYZ tristimulus values, compute a matrix <i>T</i> as follows:

<img alt="Illustration of a matrix computation" border="" src="images/6b28e3fc-d85b-4cd2-a535-522ac9f11501.gif"/>
Given <i>T</i>, you can use the following formulas to convert between an RGB color value and a CIE XYZ tristimulus value. These formulas assume that the RGB components are linear (not gamma corrected) and are normalized to the range [0...1].

<img alt="Illustration of a matrix computation" border="" src="images/5e0b7470-4123-49f4-93ed-be9955ccf825.gif"/>
To convert colors directly from one RGB color space to another, use the following formula, where <i>T1</i> is the matrix for color space RGB1, and <i>T2</i> is the matrix for color space RGB2.

<img alt="Illustration of a matrix computation" border="" src="images/3c2f9626-ef5e-4165-a24e-8720e215ef13.gif"/>
For a derivation of these formulas, refer to Charles Poynton, Digital Video and HDTV Algorithms and Interfaces (Morgan Kaufmann, 2003).

This enumeration is equivalent to the <b>DXVA_VideoPrimaries</b> enumeration used in DXVA 1.0.
      

If you are using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface to describe the video format, the color primaries are specified in the <a href="/windows/desktop/medfound/mf-mt-video-primaries-attribute">MF_MT_VIDEO_PRIMARIES</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
