---
UID: NS:xaudio2.XAUDIO2_FILTER_PARAMETERS
title: XAUDIO2_FILTER_PARAMETERS (xaudio2.h)
description: Defines filter parameters for a source voice.
helpviewer_keywords: ["XAUDIO2_FILTER_PARAMETERS","XAUDIO2_FILTER_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_filter_parameters","xaudio2/XAUDIO2_FILTER_PARAMETERS"]
old-location: xaudio2\xaudio2_filter_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_FILTER_PARAMETERS
ms.date: 12/05/2018
ms.keywords: XAUDIO2_FILTER_PARAMETERS, XAUDIO2_FILTER_PARAMETERS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_filter_parameters, xaudio2/XAUDIO2_FILTER_PARAMETERS
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
targetos: Windows
req.typenames: XAUDIO2_FILTER_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_FILTER_PARAMETERS
 - xaudio2/XAUDIO2_FILTER_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_FILTER_PARAMETERS
---

# XAUDIO2_FILTER_PARAMETERS structure


## -description

Defines filter parameters for a source voice.

## -struct-fields

### -field Type

The <a href="/windows/desktop/api/xaudio2/ne-xaudio2-xaudio2_filter_type">XAUDIO2_FILTER_TYPE</a>.

### -field Frequency

Filter radian frequency calculated as (2 * sin(pi * (desired filter cutoff frequency) / sampleRate)). The frequency must be greater than or equal to 0 and less than or equal to XAUDIO2_MAX_FILTER_FREQUENCY. The maximum frequency allowable is equal to the source sound's sample rate divided by six which corresponds to the maximum filter radian frequency of 1. For example, if a sound's sample rate is 48000 and the desired cutoff frequency is the maximum allowable value for that sample rate, 8000, the value for <b>Frequency</b> will be 1. 
If XAUDIO2_HELPER_FUNCTIONS is defined, XAudio2.h will include the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency">XAudio2RadiansToCutoffFrequency</a> and <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians">XAudio2CutoffFrequencyToRadians</a> helper functions for converting between hertz and radian frequencies. Defining XAUDIO2_HELPER_FUNCTIONS will also include <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient">XAudio2CutoffFrequencyToOnePoleCoefficient</a> for converting between hertz and a one-pole coefficient suitable for use with the LowPassOnePoleFilter and HighPassOnePoleFilter.

### -field OneOverQ

Reciprocal of Q factor. Controls how quickly frequencies beyond Frequency are dampened. Larger values result in quicker dampening while smaller values cause dampening to occur more gradually. Must be greater than 0 and less than or equal to XAUDIO2_MAX_FILTER_ONEOVERQ.

## -remarks

Setting XAUDIO2_FILTER_PARAMETERS with the following values is acoustically equivalent to the filter being fully bypassed.


```
XAUDIO2_FILTER_PARAMETERS FilterParams;
FilterParams.Frequency = 1.0f;    
FilterParams.OneOverQ = 1.0f;
FilterParams.Type = LowPassFilter;

```


The following formulas show the relationship between the members of XAUDIO2_FILTER_PARAMETERS and the per-voice filter.


```
Yl( n ) = F1 yb( n ) + yl( n - 1 )
Yb( n ) = F1 yh( n ) + yb( n - 1 )
Yh( n ) = x( n ) - yl( n ) - OneOverQ(yb( n - 1 )
Yn( n ) = Yl(n) + Yh(n)


```


Where:


```
Yl = lowpass output
Yb = bandpass output
Yh = highpass output
Yn = notch output
F1 = XAUDIO2_FILTER_PARAMETERS.Frequency
OneOverQ = XAUDIO2_FILTER_PARAMETERS.OneOverQ
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getfilterparameters">IXAudio2Voice::GetFilterParameters</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters">IXAudio2Voice::SetFilterParameters</a>



<a href="/windows/desktop/xaudio2/structures">XAudio2 Structures</a>