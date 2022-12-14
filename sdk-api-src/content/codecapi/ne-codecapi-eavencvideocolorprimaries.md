---
UID: NE:codecapi.eAVEncVideoColorPrimaries
title: eAVEncVideoColorPrimaries (codecapi.h)
description: Specifies the color primaries of the video. This enumeration is used with the AVEncVideoInputColorPrimaries and AVEncVideoOutputColorPrimaries properties.
helpviewer_keywords: ["codecapi/eAVEncVideoColorPrimaries","codecapi/eAVEncVideoColorPrimaries_BT470_2_SysBG","codecapi/eAVEncVideoColorPrimaries_BT470_2_SysM","codecapi/eAVEncVideoColorPrimaries_BT709","codecapi/eAVEncVideoColorPrimaries_EBU3231","codecapi/eAVEncVideoColorPrimaries_Reserved","codecapi/eAVEncVideoColorPrimaries_SMPTE170M","codecapi/eAVEncVideoColorPrimaries_SMPTE240M","codecapi/eAVEncVideoColorPrimaries_SMPTE_C","codecapi/eAVEncVideoColorPrimaries_SameAsSource","dshow.eavencvideocolorprimaries","eAVEncVideoColorPrimaries","eAVEncVideoColorPrimaries enumeration [DirectShow]","eAVEncVideoColorPrimariesEnumeration","eAVEncVideoColorPrimaries_BT470_2_SysBG","eAVEncVideoColorPrimaries_BT470_2_SysM","eAVEncVideoColorPrimaries_BT709","eAVEncVideoColorPrimaries_EBU3231","eAVEncVideoColorPrimaries_Reserved","eAVEncVideoColorPrimaries_SMPTE170M","eAVEncVideoColorPrimaries_SMPTE240M","eAVEncVideoColorPrimaries_SMPTE_C","eAVEncVideoColorPrimaries_SameAsSource"]
old-location: dshow\eavencvideocolorprimaries.htm
tech.root: dshow
ms.assetid: dd86a0e2-79ba-4d40-9a2f-a7dd6c6ab36d
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoColorPrimaries, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysBG, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysM, codecapi/eAVEncVideoColorPrimaries_BT709, codecapi/eAVEncVideoColorPrimaries_EBU3231, codecapi/eAVEncVideoColorPrimaries_Reserved, codecapi/eAVEncVideoColorPrimaries_SMPTE170M, codecapi/eAVEncVideoColorPrimaries_SMPTE240M, codecapi/eAVEncVideoColorPrimaries_SMPTE_C, codecapi/eAVEncVideoColorPrimaries_SameAsSource, dshow.eavencvideocolorprimaries, eAVEncVideoColorPrimaries, eAVEncVideoColorPrimaries enumeration [DirectShow], eAVEncVideoColorPrimariesEnumeration, eAVEncVideoColorPrimaries_BT470_2_SysBG, eAVEncVideoColorPrimaries_BT470_2_SysM, eAVEncVideoColorPrimaries_BT709, eAVEncVideoColorPrimaries_EBU3231, eAVEncVideoColorPrimaries_Reserved, eAVEncVideoColorPrimaries_SMPTE170M, eAVEncVideoColorPrimaries_SMPTE240M, eAVEncVideoColorPrimaries_SMPTE_C, eAVEncVideoColorPrimaries_SameAsSource
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncVideoColorPrimaries
 - codecapi/eAVEncVideoColorPrimaries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorPrimaries
---

# eAVEncVideoColorPrimaries enumeration


## -description

Specifies the color primaries of the video. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoinputcolorprimaries-property">AVEncVideoInputColorPrimaries</a> and <a href="/windows/desktop/DirectShow/avencvideooutputcolorprimaries-property">AVEncVideoOutputColorPrimaries</a> properties.

## -enum-fields

### -field eAVEncVideoColorPrimaries_SameAsSource:0

Use the same primaries as the input video. This flag applies to the <b>AVEncVideoOutputColorPrimaries</b> property only.

### -field eAVEncVideoColorPrimaries_Reserved:1

Reserved. Do not use.

### -field eAVEncVideoColorPrimaries_BT709:2

ITU-R BT.709 (including sRGB and scRGB).

### -field eAVEncVideoColorPrimaries_BT470_2_SysM:3

ITU-R.BT.470-4 System M (NTSC).

### -field eAVEncVideoColorPrimaries_BT470_2_SysBG:4

ITU-R.BT.470-4 System B,G (NTSC).

### -field eAVEncVideoColorPrimaries_SMPTE170M:5

SMPTE 170M.

### -field eAVEncVideoColorPrimaries_SMPTE240M:6

SMPTE 240M.

### -field eAVEncVideoColorPrimaries_EBU3231:7

EBU 3213.

### -field eAVEncVideoColorPrimaries_SMPTE_C:8

SPMTE C (NTSC).

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
