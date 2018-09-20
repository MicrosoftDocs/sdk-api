---
UID: NF:xaudio2.XAudio2RadiansToCutoffFrequency
title: XAudio2RadiansToCutoffFrequency function
author: windows-sdk-content
description: Inline function that converts from the radian frequencies used in XAUDIO2_FILTER_PARAMETERS back to absolute frequencies in hertz.
old-location: xaudio2\xaudio2radianstocutofffrequency.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2RadiansToCutoffFrequency(float,float)
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: XAudio2RadiansToCutoffFrequency, XAudio2RadiansToCutoffFrequency function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2radianstocutofffrequency, xaudio2/XAudio2RadiansToCutoffFrequency
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
 - XAudio2RadiansToCutoffFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XAudio2RadiansToCutoffFrequency function


## -description


Inline function that converts from the radian frequencies used in <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> back to absolute frequencies in hertz.


## -parameters




### -param Radians [in]

Value of the Frequency member of the <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure.


### -param SampleRate [in]

The sample rate of the audio data affected by the <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure.


## -returns



Returns a floating-point value that represents the frequency in hertz.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2 Functions</a>
 

 

