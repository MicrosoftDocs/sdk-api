---
UID: NF:xaudio2.XAudio2CutoffFrequencyToOnePoleCoefficient
title: XAudio2CutoffFrequencyToOnePoleCoefficient function
author: windows-sdk-content
description: Inline function that converts from filter cutoff frequencies expressed in hertz to the filter coefficients used with the Frequency member of the XAUDIO2_FILTER_PARAMETERS structure.
old-location: xaudio2\xaudio2cutofffrequencytoonepolecoefficient.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2CutoffFrequencyToOnePoleCoefficient(float,UINT32)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: XAudio2CutoffFrequencyToOnePoleCoefficient, XAudio2CutoffFrequencyToOnePoleCoefficient function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2cutofffrequencytoonepolecoefficient, xaudio2/XAudio2CutoffFrequencyToOnePoleCoefficient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAudio2CutoffFrequencyToOnePoleCoefficient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XAudio2CutoffFrequencyToOnePoleCoefficient
: 
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
 

 

