---
UID: NE:codecapi.eAVEncCommonRateControlMode
title: eAVEncCommonRateControlMode (codecapi.h)
description: Specifies the rate control mode for an encoder. This enumeration is used with the AVEncCommonRateControlMode codec property.
helpviewer_keywords: ["codecapi/eAVEncCommonRateControlMode","codecapi/eAVEncCommonRateControlMode_CBR","codecapi/eAVEncCommonRateControlMode_GlobalLowDelayVBR","codecapi/eAVEncCommonRateControlMode_GlobalVBR","codecapi/eAVEncCommonRateControlMode_LowDelayVBR","codecapi/eAVEncCommonRateControlMode_PeakConstrainedVBR","codecapi/eAVEncCommonRateControlMode_Quality","codecapi/eAVEncCommonRateControlMode_UnconstrainedVBR","dshow.eavenccommonratecontrolmode","eAVEncCommonRateControlMode","eAVEncCommonRateControlMode enumeration [DirectShow]","eAVEncCommonRateControlModeEnumeration","eAVEncCommonRateControlMode_CBR","eAVEncCommonRateControlMode_GlobalLowDelayVBR","eAVEncCommonRateControlMode_GlobalVBR","eAVEncCommonRateControlMode_LowDelayVBR","eAVEncCommonRateControlMode_PeakConstrainedVBR","eAVEncCommonRateControlMode_Quality","eAVEncCommonRateControlMode_UnconstrainedVBR"]
old-location: dshow\eavenccommonratecontrolmode.htm
tech.root: dshow
ms.assetid: 6a8e538f-3d1e-4098-a001-a623c1212450
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncCommonRateControlMode, codecapi/eAVEncCommonRateControlMode_CBR, codecapi/eAVEncCommonRateControlMode_GlobalLowDelayVBR, codecapi/eAVEncCommonRateControlMode_GlobalVBR, codecapi/eAVEncCommonRateControlMode_LowDelayVBR, codecapi/eAVEncCommonRateControlMode_PeakConstrainedVBR, codecapi/eAVEncCommonRateControlMode_Quality, codecapi/eAVEncCommonRateControlMode_UnconstrainedVBR, dshow.eavenccommonratecontrolmode, eAVEncCommonRateControlMode, eAVEncCommonRateControlMode enumeration [DirectShow], eAVEncCommonRateControlModeEnumeration, eAVEncCommonRateControlMode_CBR, eAVEncCommonRateControlMode_GlobalLowDelayVBR, eAVEncCommonRateControlMode_GlobalVBR, eAVEncCommonRateControlMode_LowDelayVBR, eAVEncCommonRateControlMode_PeakConstrainedVBR, eAVEncCommonRateControlMode_Quality, eAVEncCommonRateControlMode_UnconstrainedVBR
f1_keywords:
- codecapi/eAVEncCommonRateControlMode
dev_langs:
- c++
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
- eAVEncCommonRateControlMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncCommonRateControlMode enumeration


## -description



Specifies the rate control mode for an encoder. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avenccommonratecontrolmode-property">AVEncCommonRateControlMode</a> codec property.




## -enum-fields




### -field eAVEncCommonRateControlMode_CBR

Constant bit rate (CBR) encoding.


### -field eAVEncCommonRateControlMode_PeakConstrainedVBR

Constrained variable bit rate (VBR) encoding.


### -field eAVEncCommonRateControlMode_UnconstrainedVBR

Unconstrained VBR encoding.


### -field eAVEncCommonRateControlMode_Quality

Quality-based VBR encoding. The encoder selects the bit rate to match a specified quality level. To specify the quality level, set the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avenccommonquality-property">AVEncCommonQuality</a> property.


### -field eAVEncCommonRateControlMode_LowDelayVBR

Low delay VBR encoding. H.264 extension.

Requires Windows 8.


### -field eAVEncCommonRateControlMode_GlobalVBR

Global VBR encoding. H.264 extension.

Requires Windows 8.


### -field eAVEncCommonRateControlMode_GlobalLowDelayVBR

Global low delay VBR encoding. H.264 extension.

Requires Windows 8.


## -remarks



This enumeration is also used with <a href="https://docs.microsoft.com/windows/desktop/medfound/camera-encoder-h264-uvc-1-5">H.264 UVC 1.5 camera encoders</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

