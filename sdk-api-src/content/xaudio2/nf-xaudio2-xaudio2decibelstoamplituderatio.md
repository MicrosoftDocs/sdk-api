---
UID: NF:xaudio2.XAudio2DecibelsToAmplitudeRatio
title: XAudio2DecibelsToAmplitudeRatio function
author: windows-sdk-content
description: Inline function that converts a decibel value to an amplitude ratio value.
old-location: xaudio2\xaudio2decibelstoamplituderatio.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2DecibelsToAmplitudeRatio(float)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: XAudio2DecibelsToAmplitudeRatio, XAudio2DecibelsToAmplitudeRatio function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2decibelstoamplituderatio, xaudio2/XAudio2DecibelsToAmplitudeRatio
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
 - XAudio2DecibelsToAmplitudeRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XAudio2DecibelsToAmplitudeRatio
: 
---

# XAudio2DecibelsToAmplitudeRatio function


## -description


Inline function that converts a decibel value to an amplitude ratio value.


## -parameters




### -param Decibels [in]

Floating point value representing the decibel level.


## -returns



Returns a floating point value that represents the amplitude ratio.




## -remarks



This function can be used to calculate the Volume parameter value passed to the <a href="https://msdn.microsoft.com/en-us/library/Ee418600(v=VS.85).aspx">IXAudio2Voice::SetVolume</a> function.



You must explicitly define XAUDIO2_HELPER_FUNCTIONS in your build for this function to become available.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2 Functions</a>
 

 

