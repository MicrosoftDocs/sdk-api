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

# X3DAudioInitialize function


## -description


Sets all global 3D audio constants.


## -parameters




### -param SpeakerChannelMask [in]

Assignment of channels to speaker positions. This value must not be zero. The only permissible value on Xbox 360 is SPEAKER_XBOX.


### -param SpeedOfSound [in]

Speed of sound, in user-defined world units per second. Use this value only for doppler calculations. It must be greater than or equal to FLT_MIN.


### -param Instance [out]

3D audio instance handle. Use this handle when you call <a href="https://msdn.microsoft.com/d6b05917-9253-4c05-a318-ff13d9a329eb">X3DAudioCalculate</a>.


## -returns



This function does not return a value.




## -remarks



<b>X3DAUDIO_HANDLE</b> is an opaque data structure. Because the operating system doesn't allocate any additional storage for the 3D audio instance handle, you don't need to free or close it.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

