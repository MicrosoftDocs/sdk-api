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

# XAudio2CutoffFrequencyToOnePoleCoefficient function


## -description


Inline function that converts from filter cutoff frequencies expressed in hertz to the filter coefficients used with the <b>Frequency</b> member of the <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure.

This function applies to LowPassOnePoleFilter and HighPassOnePole filter types only, use <a href="https://msdn.microsoft.com/b46e89a9-56bc-4464-b5ab-8e618e372086">XAudio2CutoffFrequencyToRadians</a> for state-variable filter types.




## -parameters




### -param CutoffFrequency

The cutoff frequency in hertz. Frequencies greater than <i>SampleRate</i> are clamped to XAUDIO2_MAX_FILTER_FREQUENCY.


### -param SampleRate

The sample rate of the audio data affected by the <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure.


## -returns



Returns a filter coefficient for use in the <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure.






## -remarks



You must explicitly define XAUDIO2_HELPER_FUNCTIONS in your build for this function to become available.



The DirectX SDK versions of XAUDIO2 do not support one-pole filters, so this function is not present in those releases.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio::Functions</a>
 

 

