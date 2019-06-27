---
UID: NE:codecapi.eAVEncVideoColorPrimaries
title: eAVEncVideoColorPrimaries (codecapi.h)
author: windows-sdk-content
description: Specifies the color primaries of the video. This enumeration is used with the AVEncVideoInputColorPrimaries and AVEncVideoOutputColorPrimaries properties.
old-location: dshow\eavencvideocolorprimaries.htm
tech.root: DirectShow
ms.assetid: dd86a0e2-79ba-4d40-9a2f-a7dd6c6ab36d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoColorPrimaries, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysBG, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysM, codecapi/eAVEncVideoColorPrimaries_BT709, codecapi/eAVEncVideoColorPrimaries_EBU3231, codecapi/eAVEncVideoColorPrimaries_Reserved, codecapi/eAVEncVideoColorPrimaries_SMPTE170M, codecapi/eAVEncVideoColorPrimaries_SMPTE240M, codecapi/eAVEncVideoColorPrimaries_SMPTE_C, codecapi/eAVEncVideoColorPrimaries_SameAsSource, dshow.eavencvideocolorprimaries, eAVEncVideoColorPrimaries, eAVEncVideoColorPrimaries enumeration [DirectShow], eAVEncVideoColorPrimariesEnumeration, eAVEncVideoColorPrimaries_BT470_2_SysBG, eAVEncVideoColorPrimaries_BT470_2_SysM, eAVEncVideoColorPrimaries_BT709, eAVEncVideoColorPrimaries_EBU3231, eAVEncVideoColorPrimaries_Reserved, eAVEncVideoColorPrimaries_SMPTE170M, eAVEncVideoColorPrimaries_SMPTE240M, eAVEncVideoColorPrimaries_SMPTE_C, eAVEncVideoColorPrimaries_SameAsSource
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVEncVideoColorPrimaries"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorPrimaries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncVideoColorPrimaries enumeration


## -description



Specifies the color primaries of the video. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideoinputcolorprimaries-property">AVEncVideoInputColorPrimaries</a> and <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideooutputcolorprimaries-property">AVEncVideoOutputColorPrimaries</a> properties.




## -enum-fields




### -field eAVEncVideoColorPrimaries_SameAsSource

Use the same primaries as the input video. This flag applies to the <b>AVEncVideoOutputColorPrimaries</b> property only.


### -field eAVEncVideoColorPrimaries_Reserved

Reserved. Do not use.


### -field eAVEncVideoColorPrimaries_BT709

ITU-R BT.709 (including sRGB and scRGB).


### -field eAVEncVideoColorPrimaries_BT470_2_SysM

ITU-R.BT.470-4 System M (NTSC).


### -field eAVEncVideoColorPrimaries_BT470_2_SysBG

ITU-R.BT.470-4 System B,G (NTSC).


### -field eAVEncVideoColorPrimaries_SMPTE170M

SMPTE 170M.


### -field eAVEncVideoColorPrimaries_SMPTE240M

SMPTE 240M.


### -field eAVEncVideoColorPrimaries_EBU3231

EBU 3213.


### -field eAVEncVideoColorPrimaries_SMPTE_C

SPMTE C (NTSC).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

