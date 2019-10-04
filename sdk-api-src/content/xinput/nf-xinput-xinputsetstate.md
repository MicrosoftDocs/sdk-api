---
UID: NF:xinput.XInputSetState
title: XInputSetState function (xinput.h)
author: windows-sdk-content
description: Sends data to a connected controller. This function is used to activate the vibration function of a controller.
old-location: xinput\xinputsetstate.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputSetState(DWORD,XINPUT_VIBRATION*@)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XInputSetState, XInputSetState function [XInput Game Controller APIs], xinput.xinputsetstate, xinput/XInputSetState
ms.topic: function
f1_keywords:
- xinput/XInputSetState
dev_langs:
 - c++
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
req.dll: Xinput1_4.dll; Xinput9_1_0.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- xinput1_4.dll
- xinput9_1_0.dll
- Ext-MS-Win-Gaming-XInput-L1-1-0.dll
- xinputuap.dll
api_name:
- XInputSetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XInputSetState function


## -description


Sends data to a connected controller. This function is used to activate the vibration function of a controller.


## -parameters




### -param dwUserIndex [in]

Index of the user's controller. Can be a value from 0 to 3. For information about how this value is determined and how the value maps to indicators on the controller, see <a href="https://docs.microsoft.com/windows/desktop/xinput/getting-started-with-xinput">Multiple Controllers</a>.


### -param pVibration [in, out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xinput/ns-xinput-xinput_vibration">XINPUT_VIBRATION</a> structure containing the vibration information to send to the controller.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the controller is not connected, the return value is <b>ERROR_DEVICE_NOT_CONNECTED</b>.

If the function fails, the return value is an error code defined in WinError.h. The function does not use <i>SetLastError</i> to set the calling thread's last-error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xinput/ns-xinput-xinput_vibration">XINPUT_VIBRATION</a>



<a href="https://docs.microsoft.com/windows/desktop/xinput/functions">XInput Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>
 

 

