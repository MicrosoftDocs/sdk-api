---
UID: NF:xaudio2.XAudio2CutoffFrequencyToRadians
title: XAudio2CutoffFrequencyToRadians function
author: windows-sdk-content
description: Inline function that converts from filter cutoff frequencies expressed in hertz to the radian frequency values used in the Frequency member of the XAUDIO2_FILTER_PARAMETERS structure.
old-location: xaudio2\xaudio2cutofffrequencytoradians.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2CutoffFrequencyToRadians(float,UINT32)
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: XAudio2CutoffFrequencyToRadians, XAudio2CutoffFrequencyToRadians function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2cutofffrequencytoradians, xaudio2/XAudio2CutoffFrequencyToRadians
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAudio2CutoffFrequencyToRadians
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAudio2CutoffFrequencyToRadians function


## -description


Inline function that converts from filter cutoff frequencies expressed in hertz to the radian frequency values used in the <b>Frequency</b> member of the <a href="https://msdn.microsoft.com/library/Ee419237(v=VS.85).aspx">XAUDIO2_FILTER_PARAMETERS</a> structure.


## -parameters




### -param CutoffFrequency [in]

The cutoff frequency in hertz. Frequencies greater than SampleRate ÷ 6 are clamped to XAUDIO2_MAX_FILTER_FREQUENCY.


### -param SampleRate [in]

The sample rate of the audio data affected by the <a href="https://msdn.microsoft.com/library/Ee419237(v=VS.85).aspx">XAUDIO2_FILTER_PARAMETERS</a> structure.



## -returns



Returns a radian frequency for use in the <a href="https://msdn.microsoft.com/library/Ee419237(v=VS.85).aspx">XAUDIO2_FILTER_PARAMETERS</a> structure. 




## -remarks



You must explicitly define XAUDIO2_HELPER_FUNCTIONS in your build for this function to become available.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2 Functions</a>
 

 

