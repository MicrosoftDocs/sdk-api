---
UID: NF:xinput.XInputGetState
title: XInputGetState function (xinput.h)
description: Retrieves the current state of the specified controller.
helpviewer_keywords: ["XInputGetState","XInputGetState function [XInput Game Controller APIs]","xinput.xinputgetstate","xinput/XInputGetState"]
old-location: xinput\xinputgetstate.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetState(DWORD,XINPUT_STATE*@)
ms.date: 12/05/2018
ms.keywords: XInputGetState, XInputGetState function [XInput Game Controller APIs], xinput.xinputgetstate, xinput/XInputGetState
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
req.dll: Xinput1_4.dll; Xinput9_1_0.dll; Xinputuap.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XInputGetState
 - xinput/XInputGetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - xinput1_4.dll
 - xinput9_1_0.dll
 - xinputuap.dll
 - Ext-MS-Win-Gaming-XInput-L1-1-0.dll
api_name:
 - XInputGetState
---

# XInputGetState function


## -description

Retrieves the current state of the specified controller.

## -parameters

### -param dwUserIndex [in]

Index of the user's controller. Can be a value from 0 to 3. For information about how this value is determined and how the value maps to indicators on the controller, see <a href="/windows/desktop/xinput/getting-started-with-xinput">Multiple Controllers</a>.

### -param pState [out]

Pointer to an <a href="/windows/desktop/api/xinput/ns-xinput-xinput_state">XINPUT_STATE</a> structure that receives the current state of the controller.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.


If the controller is not connected, the return value is <b>ERROR_DEVICE_NOT_CONNECTED</b>.


If the function fails, the return value is an error code defined in Winerror.h. The function does not use <b>SetLastError</b> to set the calling thread's last-error code.

## -remarks

When <b>XInputGetState</b> is used to retrieve controller data, the left and right triggers are each reported separately. For legacy reasons, when DirectInput retrieves controller data, the two triggers share the same axis. The legacy behavior is noticeable in the current Game Device Control Panel, which uses DirectInput for controller state.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4), DirectX SDK (XInput 1.3), Windows Vista (XInput 9.1.0)

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/api/xinput/ns-xinput-xinput_state">XINPUT_STATE</a>



<a href="/windows/desktop/xinput/functions">XInput Functions</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a>