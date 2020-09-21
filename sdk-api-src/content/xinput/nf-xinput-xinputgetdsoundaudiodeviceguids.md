---
UID: NF:xinput.XInputGetDSoundAudioDeviceGuids
title: XInputGetDSoundAudioDeviceGuids function (xinput.h)
description: Gets the sound rendering and sound capture device GUIDs that are associated with the headset connected to the specified controller.
helpviewer_keywords: ["XInputGetDSoundAudioDeviceGuids","XInputGetDSoundAudioDeviceGuids function [XInput Game Controller APIs]","xinput.xinputgetdsoundaudiodeviceguids","xinput/XInputGetDSoundAudioDeviceGuids"]
old-location: xinput\xinputgetdsoundaudiodeviceguids.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetDSoundAudioDeviceGuids(DWORD,GUID*@,GUID*@)
ms.date: 12/05/2018
ms.keywords: XInputGetDSoundAudioDeviceGuids, XInputGetDSoundAudioDeviceGuids function [XInput Game Controller APIs], xinput.xinputgetdsoundaudiodeviceguids, xinput/XInputGetDSoundAudioDeviceGuids
req.header: xinput.h
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
req.lib: Xinput.lib; Xinput9_1_0.lib
req.dll: Xinput9_1_0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XInputGetDSoundAudioDeviceGuids
 - xinput/XInputGetDSoundAudioDeviceGuids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - xinput9_1_0.dll
api_name:
 - XInputGetDSoundAudioDeviceGuids
---

# XInputGetDSoundAudioDeviceGuids function


## -description

Gets the sound rendering and sound capture device GUIDs that are associated with the headset connected to the specified controller.

## -parameters

### -param dwUserIndex

[in] Index of the user's controller. It can be a value in the range 0–3. For information about how this value is determined and how the value maps to indicators on the controller, see <a href="/windows/desktop/xinput/getting-started-with-xinput">Multiple Controllers</a>.

### -param pDSoundRenderGuid

[out] Pointer that receives the GUID of the headset sound rendering device.

### -param pDSoundCaptureGuid

[out] Pointer that receives the GUID of the headset sound capture device.

## -returns

If the function successfully retrieves the device IDs for render and capture, the return code is <b>ERROR_SUCCESS</b>.



If there is no headset connected to the controller, the function also retrieves <b>ERROR_SUCCESS</b> with <b>GUID_NULL</b> as the values for <i>pDSoundRenderGuid</i> and <i>pDSoundCaptureGuid</i>.



If the controller port device is not physically connected, the function returns <b>ERROR_DEVICE_NOT_CONNECTED</b>.



If the function fails, it returns a valid Win32 error code.

## -remarks

Use of legacy <a href="/previous-versions/windows/desktop/ee416960(v=vs.85)">DirectSound</a> is not recommended, and DirectSound is not available for Windows Store apps.

<div class="alert"><b>Note</b>  <b>XInputGetDSoundAudioDeviceGuids</b> is deprecated because it isn't supported by Windows 8 (XInput 1.4).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
DirectX SDK (XInput 1.3), Windows Vista (XInput 9.1.0)

## -see-also

<a href="/windows/desktop/xinput/functions">XInput Functions</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>