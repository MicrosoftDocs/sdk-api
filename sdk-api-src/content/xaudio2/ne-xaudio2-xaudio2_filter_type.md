---
UID: NE:xaudio2.XAUDIO2_FILTER_TYPE
title: XAUDIO2_FILTER_TYPE
author: windows-driver-content
description: Indicates the filter type.
old-location: xaudio2\xaudio2_filter_type.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_FILTER_TYPE
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: BandPassFilter, HighPassFilter, HighPassOnePoleFilter, LowPassFilter, LowPassOnePoleFilter, NotchFilter, XAUDIO2_FILTER_TYPE, XAUDIO2_FILTER_TYPE enumeration [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_filter_type, xaudio2/BandPassFilter, xaudio2/HighPassFilter, xaudio2/HighPassOnePoleFilter, xaudio2/LowPassFilter, xaudio2/LowPassOnePoleFilter, xaudio2/NotchFilter, xaudio2/XAUDIO2_FILTER_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	xaudio2.h
api_name:
-	XAUDIO2_FILTER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAUDIO2_FILTER_TYPE enumeration


## -description


Indicates the filter type.


## -enum-fields




### -field LowPassFilter

Attenuates (reduces) frequencies above the cutoff frequency.


### -field BandPassFilter

Attenuates frequencies outside a given range.


### -field HighPassFilter

Attenuates frequencies below the cutoff frequency.


### -field NotchFilter

Attenuates frequencies inside a given range.


### -field LowPassOnePoleFilter

Attenuates frequencies above the cutoff frequency. This is a one-pole filter, and <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a>.<b>OneOverQ</b> has no effect.


### -field HighPassOnePoleFilter

Attenuates frequencies below the cutoff frequency. This is a one-pole filter, and <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a>.<b>OneOverQ</b> has no effect.


## -remarks



<div class="alert"><b>Note</b>  Note that the DirectX SDK versions of XAUDIO2 do not support the <b>LowPassOnePoleFilter</b> or the <b>HighPassOnePoleFilter</b>.    </div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a>



<a href="https://msdn.microsoft.com/7b20bda9-dab2-cfbc-125a-cf46e4ede0c8">XAudio2::Enumerations</a>
 

 

