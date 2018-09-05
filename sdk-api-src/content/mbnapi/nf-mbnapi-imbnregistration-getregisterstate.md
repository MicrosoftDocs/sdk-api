---
UID: NF:mbnapi.IMbnRegistration.GetRegisterState
title: IMbnRegistration::GetRegisterState
author: windows-sdk-content
description: Gets the registration state.
old-location: mbn\imbnregistration_getregisterstate.htm
old-project: mbn
ms.assetid: 19488f2e-0cec-4e87-a32a-274e82cd8766
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRegisterState, GetRegisterState method [Microsoft Broadband Networks], GetRegisterState method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetRegisterState method, IMbnRegistration.GetRegisterState, IMbnRegistration::GetRegisterState, mbn.imbnregistration_getregisterstate, mbnapi/IMbnRegistration::GetRegisterState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRegistration.GetRegisterState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistration::GetRegisterState


## -description


Gets the registration state.


## -parameters




### -param registerState [out]

A pointer an <a href="https://msdn.microsoft.com/cbe29357-b374-4764-9322-6308b98ddc3e">MBN_REGISTER_STATE</a> value that specifies to the current registration state of the device.  The value is meaningful only if the method returned <b>S_OK</b>. 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The registration state is not available.  The Mobile Broadband service is currently probing the device for the information.  When the registration state is available, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the registration state.

</td>
</tr>
</table>
 




## -remarks



The <b>GetRegisterState</b> method gets the current network registration state of the device.  The device can be registered to a network, searching the network for registration,  or it can be denied registration.

The registration state of device can change automatically.  For example, when the device goes out of the network coverage area, it changes the registration state from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_SEARCHING</b>.

An application can register for receiving registration state change updates by connecting <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a> interface. Windows will call the <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <b>IMbnRegistrationEvents</b> to notify the application about these changes.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>,  the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered). Then it will call the <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a>
 

 

