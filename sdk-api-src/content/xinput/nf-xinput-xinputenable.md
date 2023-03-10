---
UID: NF:xinput.XInputEnable
title: XInputEnable function (xinput.h)
description: Sets the reporting state of XInput.
helpviewer_keywords: ["XInputEnable","XInputEnable function [XInput Game Controller APIs]","xinput.xinputenable","xinput/XInputEnable"]
old-location: xinput\xinputenable.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputEnable(BOOL)
ms.date: 12/05/2018
ms.keywords: XInputEnable, XInputEnable function [XInput Game Controller APIs], xinput.xinputenable, xinput/XInputEnable
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
req.lib: Xinput.lib
req.dll: Xinput1_4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XInputEnable
 - xinput/XInputEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - xinput1_4.dll
 - Ext-MS-Win-Gaming-XInput-L1-1-0.dll
 - xinputuap.dll
api_name:
 - XInputEnable
---

# XInputEnable function


## -description

Sets the reporting state of XInput.

## -parameters

### -param enable [in]

If enable is <b>FALSE</b>, XInput will only send neutral data in response to <a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a> (all buttons up, axes centered, and triggers at 0). <a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a> calls will be registered but not sent to the device. Sending any value other than <b>FALSE </b> will restore reading and writing functionality to normal.

## -remarks

This function is meant to be called when an application gains or loses focus (such as via <a href="/windows/desktop/winmsg/wm-activateapp">WM_ACTIVATEAPP</a>). Using this function, you will not have to change the XInput query loop in your application as neutral data will always be reported if XInput is disabled.


In a controller that supports vibration effects:

<ul>
<li>Passing <b>FALSE</b> will stop any vibration effects currently playing. In this state, calls to <a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a> will be registered, but not passed to the device.</li>
<li>Passing <b>TRUE</b> will pass the last vibration request (even if it is 0) sent to <a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a> to the device.</li>
</ul>

**Windows 10 or later:** *Deprecated*, as game controller input is automatically enabled/disabled by the system based on the application window focus.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4), DirectX SDK (XInput 1.3)

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/api/xinput/ns-xinput-xinput_state">XINPUT_STATE</a>



<a href="/windows/desktop/xinput/functions">XInput Functions</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a>
