---
UID: NF:xinput.XInputEnable
title: XInputEnable function
author: windows-sdk-content
description: Sets the reporting state of XInput.
old-location: xinput\xinputenable.htm
old-project: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputEnable(BOOL)
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: XInputEnable, XInputEnable function [XInput Game Controller APIs], xinput.xinputenable, xinput/XInputEnable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
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
product: Windows
targetos: Windows
req.lib: Xinput.lib
req.dll: Xinput1_4.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XInputEnable function


## -description


Sets the reporting state of XInput.


## -parameters




### -param enable [in]

If enable is <b>FALSE</b>, XInput will only send neutral data in response to <a href="https://msdn.microsoft.com/D261219D-0175-4690-8F1F-BDAACE2E7424">XInputGetState</a> (all buttons up, axes centered, and triggers at 0). <a href="https://msdn.microsoft.com/FA494AEB-9FB9-4AF4-95AB-01048A60D924">XInputSetState</a> calls will be registered but not sent to the device. Sending any value other than <b>FALSE </b>will restore reading and writing functionality to normal.


## -returns



This function does not return a value.




## -remarks



This function is meant to be called when an application gains or loses focus (such as via <a href="https://msdn.microsoft.com/fc3626ac-8f19-4aa6-8fe9-5020d00c09db">WM_ACTIVATEAPP</a>). Using this function, you will not have to change the XInput query loop in your application as neutral data will always be reported if XInput is disabled.


In a controller that supports vibration effects:

<ul>
<li>Passing <b>FALSE</b> will stop any vibration effects currently playing. In this state, calls to <a href="https://msdn.microsoft.com/FA494AEB-9FB9-4AF4-95AB-01048A60D924">XInputSetState</a> will be registered, but not passed to the device.</li>
<li>Passing <b>TRUE</b> will pass the last vibration request (even if it is 0) sent to <a href="https://msdn.microsoft.com/FA494AEB-9FB9-4AF4-95AB-01048A60D924">XInputSetState</a> to the device.</li>
</ul>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8 (XInput 1.4), DirectX SDK (XInput 1.3)




## -see-also




<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a>



<a href="https://msdn.microsoft.com/1EBFB5FF-3DAA-43D8-AADA-5FFEED56F79D">XINPUT_STATE</a>



<a href="https://msdn.microsoft.com/c1533555-9094-0030-f025-6f47e9002e1a">XInput Functions</a>



<a href="https://msdn.microsoft.com/D261219D-0175-4690-8F1F-BDAACE2E7424">XInputGetState</a>



<a href="https://msdn.microsoft.com/FA494AEB-9FB9-4AF4-95AB-01048A60D924">XInputSetState</a>
 

 

