---
UID: NF:xinput.XInputGetKeystroke
title: XInputGetKeystroke function (xinput.h)
description: Retrieves a gamepad input event.
helpviewer_keywords: ["XInputGetKeystroke","XInputGetKeystroke function [XInput Game Controller APIs]","xinput.xinputgetkeystroke","xinput/XInputGetKeystroke"]
old-location: xinput\xinputgetkeystroke.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetKeystroke(DWORD,DWORD,PXINPUT_KEYSTROKE@)
ms.date: 12/05/2018
ms.keywords: XInputGetKeystroke, XInputGetKeystroke function [XInput Game Controller APIs], xinput.xinputgetkeystroke, xinput/XInputGetKeystroke
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
 - XInputGetKeystroke
 - xinput/XInputGetKeystroke
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
 - XInputGetKeystroke
---

# XInputGetKeystroke function


## -description

Retrieves a gamepad input event.

## -parameters

### -param dwUserIndex

[in] Index of the signed-in gamer associated with the device. Can be a value in the range 0–XUSER_MAX_COUNT − 1, or XUSER_INDEX_ANY to fetch the next available input event from any user.

### -param dwReserved

[in] Reserved

### -param pKeystroke

[out] Pointer to an <a href="/windows/desktop/api/xinput/ns-xinput-xinput_keystroke">XINPUT_KEYSTROKE</a> structure that receives an input event.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.


If no new keys have been pressed, the return value is <b>ERROR_EMPTY</b>.


If the controller is not connected or the user has not activated it, the return value is <b>ERROR_DEVICE_NOT_CONNECTED</b>. See the Remarks section below.

If the function fails, the return value is an error code defined in Winerror.h. The function does not use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set the calling thread's last-error code.

## -remarks

Wireless controllers are not considered active upon system startup, and calls to any of the <i>XInput</i> functions before a wireless controller is made active return <b>ERROR_DEVICE_NOT_CONNECTED</b>. Game titles must examine the return code and be prepared to handle this condition. Wired controllers are automatically activated when they are inserted. Wireless controllers are activated when the user power on the controller.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4), DirectX SDK (XInput 1.3)

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_keystroke">XINPUT_KEYSTROKE</a>



<a href="/windows/desktop/xinput/functions">XInput Functions</a>