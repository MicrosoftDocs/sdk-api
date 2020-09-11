---
UID: NE:mfobjects._MFVideoTransferFunction
title: MFVideoTransferFunction (mfobjects.h)
description: Specifies the conversion function from linear RGB to non-linear RGB (R'G'B').
helpviewer_keywords: ["MFVideoTransFunc_10","MFVideoTransFunc_18","MFVideoTransFunc_20","MFVideoTransFunc_2020","MFVideoTransFunc_2020_const","MFVideoTransFunc_2084","MFVideoTransFunc_22","MFVideoTransFunc_240M","MFVideoTransFunc_26","MFVideoTransFunc_28","MFVideoTransFunc_709","MFVideoTransFunc_709_sym","MFVideoTransFunc_ForceDWORD","MFVideoTransFunc_HLG","MFVideoTransFunc_Last","MFVideoTransFunc_Log_100","MFVideoTransFunc_Log_316","MFVideoTransFunc_Unknown","MFVideoTransFunc_sRGB","MFVideoTransferFunction","MFVideoTransferFunction enumeration [Media Foundation]","f9aff1d5-e9f7-48fd-9c86-8dc597d37dfa","mf.mfvideotransferfunction","mfobjects/MFVideoTransFunc_10","mfobjects/MFVideoTransFunc_18","mfobjects/MFVideoTransFunc_20","mfobjects/MFVideoTransFunc_2020","mfobjects/MFVideoTransFunc_2020_const","mfobjects/MFVideoTransFunc_2084","mfobjects/MFVideoTransFunc_22","mfobjects/MFVideoTransFunc_240M","mfobjects/MFVideoTransFunc_26","mfobjects/MFVideoTransFunc_28","mfobjects/MFVideoTransFunc_709","mfobjects/MFVideoTransFunc_709_sym","mfobjects/MFVideoTransFunc_ForceDWORD","mfobjects/MFVideoTransFunc_HLG","mfobjects/MFVideoTransFunc_Last","mfobjects/MFVideoTransFunc_Log_100","mfobjects/MFVideoTransFunc_Log_316","mfobjects/MFVideoTransFunc_Unknown","mfobjects/MFVideoTransFunc_sRGB","mfobjects/MFVideoTransferFunction"]
old-location: mf\mfvideotransferfunction.htm
tech.root: mf
ms.assetid: f9aff1d5-e9f7-48fd-9c86-8dc597d37dfa
ms.date: 12/05/2018
ms.keywords: MFVideoTransFunc_10, MFVideoTransFunc_18, MFVideoTransFunc_20, MFVideoTransFunc_2020, MFVideoTransFunc_2020_const, MFVideoTransFunc_2084, MFVideoTransFunc_22, MFVideoTransFunc_240M, MFVideoTransFunc_26, MFVideoTransFunc_28, MFVideoTransFunc_709, MFVideoTransFunc_709_sym, MFVideoTransFunc_ForceDWORD, MFVideoTransFunc_HLG, MFVideoTransFunc_Last, MFVideoTransFunc_Log_100, MFVideoTransFunc_Log_316, MFVideoTransFunc_Unknown, MFVideoTransFunc_sRGB, MFVideoTransferFunction, MFVideoTransferFunction enumeration [Media Foundation], f9aff1d5-e9f7-48fd-9c86-8dc597d37dfa, mf.mfvideotransferfunction, mfobjects/MFVideoTransFunc_10, mfobjects/MFVideoTransFunc_18, mfobjects/MFVideoTransFunc_20, mfobjects/MFVideoTransFunc_2020, mfobjects/MFVideoTransFunc_2020_const, mfobjects/MFVideoTransFunc_2084, mfobjects/MFVideoTransFunc_22, mfobjects/MFVideoTransFunc_240M, mfobjects/MFVideoTransFunc_26, mfobjects/MFVideoTransFunc_28, mfobjects/MFVideoTransFunc_709, mfobjects/MFVideoTransFunc_709_sym, mfobjects/MFVideoTransFunc_ForceDWORD, mfobjects/MFVideoTransFunc_HLG, mfobjects/MFVideoTransFunc_Last, mfobjects/MFVideoTransFunc_Log_100, mfobjects/MFVideoTransFunc_Log_316, mfobjects/MFVideoTransFunc_Unknown, mfobjects/MFVideoTransFunc_sRGB, mfobjects/MFVideoTransferFunction
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
req.typenames: MFVideoTransferFunction
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoTransferFunction
 - mfobjects/_MFVideoTransferFunction
 - MFVideoTransferFunction
 - mfobjects/MFVideoTransferFunction
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
 - MFVideoTransferFunction
---

# MFVideoTransferFunction enumeration


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

These flags are used with the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-transfer-function-attribute">MF_MT_TRANSFER_FUNCTION</a> attribute.
      

For more information about these values, see the remarks for the <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videotransferfunction">DXVA2_VideoTransferFunction</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-media-types">Video Media Types</a>

