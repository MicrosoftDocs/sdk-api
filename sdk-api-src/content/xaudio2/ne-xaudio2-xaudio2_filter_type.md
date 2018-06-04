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
 

 

