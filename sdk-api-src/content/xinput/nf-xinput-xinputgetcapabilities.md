---
UID: NF:xinput.XInputGetCapabilities
title: XInputGetCapabilities function (xinput.h)
description: Retrieves the capabilities and features of a connected controller.
helpviewer_keywords: ["XInputGetCapabilities","XInputGetCapabilities function [XInput Game Controller APIs]","xinput.xinputgetcapabilities","xinput/XInputGetCapabilities"]
old-location: xinput\xinputgetcapabilities.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetCapabilities(DWORD,DWORD,XINPUT_CAPABILITIES*@)
ms.date: 12/05/2018
ms.keywords: XInputGetCapabilities, XInputGetCapabilities function [XInput Game Controller APIs], xinput.xinputgetcapabilities, xinput/XInputGetCapabilities
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XInputGetCapabilities
 - xinput/XInputGetCapabilities
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
 - Ext-MS-Win-Gaming-XInput-L1-1-0.dll
 - xinputuap.dll
api_name:
 - XInputGetCapabilities
---

# XInputGetCapabilities function


## -description

Retrieves the capabilities and features of a connected controller.

## -parameters

### -param dwUserIndex [in]

Index of the user's controller. Can be a value in the range 0–3. For information about how this value is determined and how the value maps to indicators on the controller, see <a href="/windows/desktop/xinput/getting-started-with-xinput">Multiple Controllers</a>.

### -param dwFlags [in]

Input flags that identify the controller type. If this value is 0, then the capabilities of all controllers connected to the system are returned. Currently, only one value is supported:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>XINPUT_FLAG_GAMEPAD</b></td>
<td>Limit query to devices of controller type.</td>
</tr>
</table>
 

Any value of <i>dwflags</i> other than the above or 0 is illegal and will result in an error break when debugging.

### -param pCapabilities [out]

Pointer to an <a href="/windows/desktop/api/xinput/ns-xinput-xinput_capabilities">XINPUT_CAPABILITIES</a> structure that receives the controller capabilities.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.


If the controller is not connected, the return value is <b>ERROR_DEVICE_NOT_CONNECTED</b>.


If the function fails, the return value is an error code defined in WinError.h. The function does not use <i>SetLastError</i> to set the calling thread's last-error code.

## -remarks

<div class="alert"><b>Note</b>  The legacy XINPUT 9.1.0 version (included in Windows Vista and later) always returned a fixed set of capabilities regardless of attached device.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4), DirectX SDK (XInput 1.3), Windows Vista (XInput 9.1.0)

## -see-also

<a href="/windows/desktop/xinput/functions">XInput Functions</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a>