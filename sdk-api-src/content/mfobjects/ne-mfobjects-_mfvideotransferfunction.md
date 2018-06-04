---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MFVideoTransferFunction enumeration


## -description



          Specifies the conversion function from linear RGB to non-linear RGB (R'G'B').
        


## -enum-fields




### -field MFVideoTransFunc_Unknown


            Unknown. Treat as MFVideoTransFunc_709.
          


### -field MFVideoTransFunc_10


            Linear RGB (gamma = 1.0).
          


### -field MFVideoTransFunc_18


            True 1.8 gamma, L' = L^1/1.8.
          


### -field MFVideoTransFunc_20


            True 2.0 gamma, L' = L^1/2.0.
          


### -field MFVideoTransFunc_22


            True 2.2 gamma, L' = L^1/2.2. This transfer function is used in ITU-R BT.470-2 System M (NTSC).
          


### -field MFVideoTransFunc_709


            ITU-R BT.709 transfer function. Gamma 2.2 curve with a linear segment in the lower range. This transfer function is used in BT.709, BT.601, SMPTE 296M, SMPTE 170M, BT.470, and SPMTE 274M. In addition BT-1361 uses this function within the range [0...1].
          


### -field MFVideoTransFunc_240M


            SPMTE 240M transfer function. Gamma 2.2 curve with a linear segment in the lower range.
          


### -field MFVideoTransFunc_sRGB


            sRGB transfer function. Gamma 2.4 curve with a linear segment in the lower range.
          


### -field MFVideoTransFunc_28


            True 2.8 gamma. L' = L^1/2.8. This transfer function is used in ITU-R BT.470-2 System B, G (PAL).
          


### -field MFVideoTransFunc_Log_100

Logarithmic transfer (100:1 range); for example, as used in H.264 video.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFVideoTransFunc_Log_316

Logarithmic transfer (316.22777:1 range); for example, as used in H.264 video.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFVideoTransFunc_709_sym

Symmetric ITU-R BT.709.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFVideoTransFunc_2020_const

Constant luminance ITU-R BT.2020.  See <a href="https://www.itu.int/dms_pubrec/itu-r/rec/bt/R-REC-BT.2020-2-201510-I!!PDF-E.pdf">Recommendation  ITU-R  BT.2020-2</a>.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

### -field MFVideoTransFunc_2020

Non-constant luminance ITU-R BT.2020.  See <a href="https://www.itu.int/dms_pubrec/itu-r/rec/bt/R-REC-BT.2020-2-201510-I!!PDF-E.pdf">Recommendation  ITU-R  BT.2020-2</a>.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

### -field MFVideoTransFunc_26

True 2.6 gamma, L’=L^1/2.6

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

### -field MFVideoTransFunc_2084

SMPTE ST.2084 also known as PQ.  Also defined in ITU-R BT.2100

<div class="alert"><b>Note</b>  Requires Windows 10, version 1703 or later.</div>
<div> </div>

### -field MFVideoTransFunc_HLG

Hybrid Log-Gamma, ARIB STD-B67

<div class="alert"><b>Note</b>  Requires Windows 10, version 1703 or later.</div>
<div> </div>

### -field MFVideoTransFunc_10_rel


### -field MFVideoTransFunc_Last


            Reserved.
          


### -field MFVideoTransFunc_ForceDWORD


            Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.
          


## -remarks




        These flags are used with the <a href="https://msdn.microsoft.com/c64c2135-f588-4d7a-9ca8-ae4f7b290572">MF_MT_TRANSFER_FUNCTION</a> attribute.
      


        For more information about these values, see the remarks for the <a href="https://msdn.microsoft.com/43b99d5f-ea28-4de2-b118-e2277f283dee">DXVA2_VideoTransferFunction</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.
      




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

