---
UID: NE:dxva2api._DXVA2_VideoTransferFunction
title: "_DXVA2_VideoTransferFunction"
author: windows-driver-content
description: Specifies the conversion function from linear RGB to non-linear RGB (R'G'B').
old-location: mf\dxva2_videotransferfunction.htm
old-project: medfound
ms.assetid: 43b99d5f-ea28-4de2-b118-e2277f283dee
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 43b99d5f-ea28-4de2-b118-e2277f283dee, DXVA2_VideoTransFuncMask, DXVA2_VideoTransFunc_10, DXVA2_VideoTransFunc_18, DXVA2_VideoTransFunc_20, DXVA2_VideoTransFunc_22, DXVA2_VideoTransFunc_240M, DXVA2_VideoTransFunc_28, DXVA2_VideoTransFunc_709, DXVA2_VideoTransFunc_Unknown, DXVA2_VideoTransFunc_sRGB, DXVA2_VideoTransferFunction, DXVA2_VideoTransferFunction enumeration [Media Foundation], _DXVA2_VideoTransferFunction, dxva2api/DXVA2_VideoTransFuncMask, dxva2api/DXVA2_VideoTransFunc_10, dxva2api/DXVA2_VideoTransFunc_18, dxva2api/DXVA2_VideoTransFunc_20, dxva2api/DXVA2_VideoTransFunc_22, dxva2api/DXVA2_VideoTransFunc_240M, dxva2api/DXVA2_VideoTransFunc_28, dxva2api/DXVA2_VideoTransFunc_709, dxva2api/DXVA2_VideoTransFunc_Unknown, dxva2api/DXVA2_VideoTransFunc_sRGB, dxva2api/DXVA2_VideoTransferFunction, mf.dxva2_videotransferfunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: DXVA2_VideoTransferFunction
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva2api.h
api_name:
-	DXVA2_VideoTransferFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA2_VideoTransferFunction enumeration


## -description


Specifies the conversion function from linear RGB to non-linear RGB (R'G'B'). These flags are used in the DXVA2_ExtendedFormat Structure.
        
      


## -enum-fields




### -field DXVA2_VideoTransFuncMask


            Bitmask to validate flag values. This value is not a valid flag.
          


### -field DXVA2_VideoTransFunc_Unknown


            Unknown. Treat as DXVA2_VideoTransFunc_709.
          


### -field DXVA2_VideoTransFunc_10


            Linear RGB (gamma = 1.0).
          


### -field DXVA2_VideoTransFunc_18


            True 1.8 gamma, L' = L^1/1.8.
          


### -field DXVA2_VideoTransFunc_20


            True 2.0 gamma, L' = L^1/2.0.
          


### -field DXVA2_VideoTransFunc_22


            True 2.2 gamma, L' = L^1/2.2. This transfer function is used in ITU-R BT.470-2 System M (NTSC).
          


### -field DXVA2_VideoTransFunc_709

ITU-R BT.709 transfer function. Gamma 2.2 curve with a linear segment in the lower range. This transfer function is used in BT.709, BT.601, SMPTE 296M, SMPTE 170M, BT.470, and SMPTE 274M. In addition BT-1361 uses this function within the range [0...1].


### -field DXVA2_VideoTransFunc_240M


            SMPTE 240M transfer function. Gamma 2.2 curve with a linear segment in the lower range.
          


### -field DXVA2_VideoTransFunc_sRGB


            sRGB transfer function. Gamma 2.4 curve with a linear segment in the lower range.
          


### -field DXVA2_VideoTransFunc_28


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

If you are using the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface to describe the video format, the transfer function is specified in the <a href="https://msdn.microsoft.com/c64c2135-f588-4d7a-9ca8-ae4f7b290572">MF_MT_TRANSFER_FUNCTION</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

