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

# X3DAUDIO_CONE structure


## -description


Specifies directionality for a single-channel non-LFE emitter by scaling DSP behavior with respect to the emitter's orientation.


## -struct-fields




### -field InnerAngle

Inner cone angle in radians. This value must be within 0.0f to X3DAUDIO_2PI.


### -field OuterAngle

Outer cone angle in radians. This value must be within <i>InnerAngle</i> to X3DAUDIO_2PI.


### -field InnerVolume

Volume scaler on/within inner cone. This value must be within 0.0f to 2.0f. 


### -field OuterVolume

Volume scaler on/beyond outer cone. This value must be within 0.0f to 2.0f. 


### -field InnerLPF

LPF direct-path or reverb-path coefficient scaler on/within inner cone. This value is only used for LPF calculations and must be within 0.0f to 1.0f. 


### -field OuterLPF

LPF direct-path or reverb-path coefficient scaler on or beyond outer cone. This value is only used for LPF calculations and must be within 0.0f to 1.0f. 


### -field InnerReverb

Reverb send level scaler on or within inner cone. This must be within 0.0f to 2.0f. 


### -field OuterReverb

Reverb send level scaler on/beyond outer cone. This must be within 0.0f to 2.0f. 



## -remarks



For a detailed explanation of sound cones see <a href="https://msdn.microsoft.com/15252358-d932-22f4-f13a-8e4b8487dd86">Sound Cones</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

