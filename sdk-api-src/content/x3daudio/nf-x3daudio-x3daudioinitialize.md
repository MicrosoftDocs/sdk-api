---
UID: NF:x3daudio.X3DAudioInitialize
title: X3DAudioInitialize function
author: windows-sdk-content
description: Sets all global 3D audio constants.
old-location: xaudio2\x3daudioinitialize.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.x3daudio.X3DAudioInitialize(UINT32,FLOAT32,X3DAUDIO_HANDLE@)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: X3DAudioInitialize, X3DAudioInitialize function [XAudio2 Audio Mixing APIs], x3daudio/X3DAudioInitialize, xaudio2.x3daudioinitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: x3daudio.h
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
req.lib: XAudio2.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - XAudio2.lib
 - XAudio2.dll
api_name:
 - X3DAudioInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- X3DAudioInitialize
: 
---

# X3DAudioInitialize function


## -description


Sets all global 3D audio constants.


## -parameters




### -param SpeakerChannelMask [in]

Assignment of channels to speaker positions. This value must not be zero. The only permissible value on Xbox 360 is SPEAKER_XBOX.


### -param SpeedOfSound [in]

Speed of sound, in user-defined world units per second. Use this value only for doppler calculations. It must be greater than or equal to FLT_MIN.


### -param Instance [out]

3D audio instance handle. Use this handle when you call <a href="https://msdn.microsoft.com/en-us/library/Ee419052(v=VS.85).aspx">X3DAudioCalculate</a>.


## -returns



This function does not return a value.




## -remarks



<b>X3DAUDIO_HANDLE</b> is an opaque data structure. Because the operating system doesn't allocate any additional storage for the 3D audio instance handle, you don't need to free or close it.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">Functions</a>
 

 

