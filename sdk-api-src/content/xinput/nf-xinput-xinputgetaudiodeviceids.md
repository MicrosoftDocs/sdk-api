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

# XInputGetAudioDeviceIds function


## -description


Retrieves the sound rendering and sound capture audio device IDs that are associated with the headset connected to the specified controller.


## -parameters




### -param dwUserIndex [in]


Index of the gamer associated with the device.


### -param pRenderDeviceId [out, optional]


Windows Core Audio device ID string for render (speakers).


### -param pRenderCount [in, out, optional]


Size, in wide-chars, of the render device ID string buffer.


### -param pCaptureDeviceId [out, optional]

Windows Core Audio device ID string for capture (microphone).


### -param pCaptureCount [in, out, optional]

Size, in wide-chars, of capture device ID string buffer.


## -returns



If the function successfully retrieves the device IDs for render and capture, the return code is <b>ERROR_SUCCESS</b>.


If there is no headset connected to the controller, the function will also retrieve <b>ERROR_SUCCESS</b> with <b>NULL</b> as the values for <i>pRenderDeviceId</i> and <i>pCaptureDeviceId</i>.


If the controller port device is not physically connected, the function will return <b>ERROR_DEVICE_NOT_CONNECTED</b>.


If the function fails, it will return a valid Win32 error code.





## -remarks



Callers must allocate the memory for the buffers passed to <b>XInputGetAudioDeviceIds</b>. The resulting strings can be of arbitrary length.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4)




## -see-also




<a href="https://msdn.microsoft.com/87ca9a31-1bc8-47ea-be00-40159d30e189">Core Audio APIs</a>



<a href="https://msdn.microsoft.com/c1533555-9094-0030-f025-6f47e9002e1a">XInput Functions</a>



<a href="https://msdn.microsoft.com/31E399C8-9001-4726-BDBA-422EF2D48E3B">XInputGetDSoundAudioDeviceGuids</a>
 

 

