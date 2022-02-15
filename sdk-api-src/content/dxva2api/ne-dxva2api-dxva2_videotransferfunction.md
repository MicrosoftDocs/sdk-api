---
UID: NE:dxva2api._DXVA2_VideoTransferFunction
title: DXVA2_VideoTransferFunction (dxva2api.h)
description: Specifies the conversion function from linear RGB to non-linear RGB (R'G'B').
helpviewer_keywords: ["43b99d5f-ea28-4de2-b118-e2277f283dee","DXVA2_VideoTransFuncMask","DXVA2_VideoTransFunc_10","DXVA2_VideoTransFunc_18","DXVA2_VideoTransFunc_20","DXVA2_VideoTransFunc_22","DXVA2_VideoTransFunc_240M","DXVA2_VideoTransFunc_28","DXVA2_VideoTransFunc_709","DXVA2_VideoTransFunc_Unknown","DXVA2_VideoTransFunc_sRGB","DXVA2_VideoTransferFunction","DXVA2_VideoTransferFunction enumeration [Media Foundation]","dxva2api/DXVA2_VideoTransFuncMask","dxva2api/DXVA2_VideoTransFunc_10","dxva2api/DXVA2_VideoTransFunc_18","dxva2api/DXVA2_VideoTransFunc_20","dxva2api/DXVA2_VideoTransFunc_22","dxva2api/DXVA2_VideoTransFunc_240M","dxva2api/DXVA2_VideoTransFunc_28","dxva2api/DXVA2_VideoTransFunc_709","dxva2api/DXVA2_VideoTransFunc_Unknown","dxva2api/DXVA2_VideoTransFunc_sRGB","dxva2api/DXVA2_VideoTransferFunction","mf.dxva2_videotransferfunction"]
old-location: mf\dxva2_videotransferfunction.htm
tech.root: mf
ms.assetid: 43b99d5f-ea28-4de2-b118-e2277f283dee
ms.date: 12/05/2018
ms.keywords: 43b99d5f-ea28-4de2-b118-e2277f283dee, DXVA2_VideoTransFuncMask, DXVA2_VideoTransFunc_10, DXVA2_VideoTransFunc_18, DXVA2_VideoTransFunc_20, DXVA2_VideoTransFunc_22, DXVA2_VideoTransFunc_240M, DXVA2_VideoTransFunc_28, DXVA2_VideoTransFunc_709, DXVA2_VideoTransFunc_Unknown, DXVA2_VideoTransFunc_sRGB, DXVA2_VideoTransferFunction, DXVA2_VideoTransferFunction enumeration [Media Foundation], dxva2api/DXVA2_VideoTransFuncMask, dxva2api/DXVA2_VideoTransFunc_10, dxva2api/DXVA2_VideoTransFunc_18, dxva2api/DXVA2_VideoTransFunc_20, dxva2api/DXVA2_VideoTransFunc_22, dxva2api/DXVA2_VideoTransFunc_240M, dxva2api/DXVA2_VideoTransFunc_28, dxva2api/DXVA2_VideoTransFunc_709, dxva2api/DXVA2_VideoTransFunc_Unknown, dxva2api/DXVA2_VideoTransFunc_sRGB, dxva2api/DXVA2_VideoTransferFunction, mf.dxva2_videotransferfunction
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
req.typenames: DXVA2_VideoTransferFunction
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoTransferFunction
 - dxva2api/_DXVA2_VideoTransferFunction
 - DXVA2_VideoTransferFunction
 - dxva2api/DXVA2_VideoTransferFunction
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
 - DXVA2_VideoTransferFunction
---

# DXVA2_VideoTransferFunction enumeration


## -description

Specifies the conversion function from linear RGB to non-linear RGB (R'G'B'). These flags are used in the DXVA2_ExtendedFormat Structure.

## -enum-fields

### -field DXVA2_VideoTransFuncMask:0x1f

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_VideoTransFunc_Unknown:0

Unknown. Treat as DXVA2_VideoTransFunc_709.

### -field DXVA2_VideoTransFunc_10:1

Linear RGB (gamma = 1.0).

### -field DXVA2_VideoTransFunc_18:2

True 1.8 gamma, L' = L^1/1.8.

### -field DXVA2_VideoTransFunc_20:3

True 2.0 gamma, L' = L^1/2.0.

### -field DXVA2_VideoTransFunc_22:4

True 2.2 gamma, L' = L^1/2.2. This transfer function is used in ITU-R BT.470-2 System M (NTSC).

### -field DXVA2_VideoTransFunc_709:5

ITU-R BT.709 transfer function. Gamma 2.2 curve with a linear segment in the lower range. This transfer function is used in BT.709, BT.601, SMPTE 296M, SMPTE 170M, BT.470, and SMPTE 274M. In addition BT-1361 uses this function within the range [0...1].

### -field DXVA2_VideoTransFunc_240M:6

SMPTE 240M transfer function. Gamma 2.2 curve with a linear segment in the lower range.

### -field DXVA2_VideoTransFunc_sRGB:7

sRGB transfer function. Gamma 2.4 curve with a linear segment in the lower range.

### -field DXVA2_VideoTransFunc_28:8

True 2.8 gamma. L' = L^1/2.8. This transfer function is used in ITU-R BT.470-2 System B, G (PAL).

## -remarks

The following table shows the formulas for the most common transfer functions. In these formulas, L is the linear value and L' is the non-linear (gamma corrected) value. These values are relative to a normalized range [0...1].

<table>
<tr>
<th>Color space</th>
<th>Transfer function</th>
</tr>
<tr>
<td>sRGB (8-bit)</td>
<td>
L' = 12.92L, for L &lt; 0.031308

L' = 1.055L^1/2.4− 0.055, for L &gt;= 0.031308

</td>
</tr>
<tr>
<td>BT.470-2 System B, G</td>
<td>L' = L^0.36</td>
</tr>
<tr>
<td>BT.470-2 System M</td>
<td>L' = L^0.45</td>
</tr>
<tr>
<td>BT.709</td>
<td>
L' = 4.50L, for L &lt; 0.018

L' = 1.099L^0.45− 0.099, for L &gt;= 0.018

</td>
</tr>
<tr>
<td>scRGB</td>
<td>L' = L</td>
</tr>
<tr>
<td>SMPTE 240M</td>
<td>
L' = 4.0L, for L &lt; 0.0228

L' = 1.1115L^0.45− 0.01115, for L &gt;= 0.0228

</td>
</tr>
</table>
 

The following table shows the inverse formulas to obtain the original gamma-corrected values:

<table>
<tr>
<th>Color space</th>
<th>Transfer function</th>
</tr>
<tr>
<td>sRGB (8-bit)</td>
<td>
L = 1/12.92L', for L' &lt; 0.03928

L = ((L' + 0.055)/1055)^2.4, for L' &gt;= 0.03928

</td>
</tr>
<tr>
<td>BT.470-2 System B, G</td>
<td>L = L'^1/0.36</td>
</tr>
<tr>
<td>BT.470-2 System M</td>
<td>L = L'^1/0.45</td>
</tr>
<tr>
<td>BT.709</td>
<td>
L = L'/4.50, for L' &lt; 0.081

L = ((L' + 0.099) / 1.099)^1/0.45, for L' &gt;= 0.081

</td>
</tr>
<tr>
<td>scRGB</td>
<td>L = L'</td>
</tr>
<tr>
<td>SMPTE 240M</td>
<td>
L = L'/4.0, for L' &lt; 0.0913

L= ((L' + 0.1115)/1.1115)^1/0.45, for L' &gt;= 0.0913

</td>
</tr>
</table>
 

This enumeration is equivalent to the <b>DXVA_VideoTransferFunction</b> enumeration used in DXVA 1.0.

If you are using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface to describe the video format, the transfer function is specified in the <a href="/windows/desktop/medfound/mf-mt-transfer-function-attribute">MF_MT_TRANSFER_FUNCTION</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
