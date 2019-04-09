---
UID: NF:mbnapi.IMbnRegistration.GetRegisterMode
title: IMbnRegistration::GetRegisterMode (mbnapi.h)
author: windows-sdk-content
description: Gets the network registration mode of a Mobile Broadband device.
old-location: mbn\imbnregistration_getregistermode.htm
tech.root: mbn
ms.assetid: 30030eb8-3b08-4583-a7ba-0560db32007f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRegisterMode, GetRegisterMode method [Microsoft Broadband Networks], GetRegisterMode method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetRegisterMode method, IMbnRegistration.GetRegisterMode, IMbnRegistration::GetRegisterMode, mbn.imbnregistration_getregistermode, mbnapi/IMbnRegistration::GetRegisterMode
ms.topic: method
req.header: mbnapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRegistration.GetRegisterMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnRegistration::GetRegisterMode


## -description


Gets the network registration mode of a Mobile Broadband device.


## -parameters




### -param registerMode [out]

A pointer to a <a href="https://msdn.microsoft.com/be64aa55-5a31-4909-9f34-634f7b14fc30">MBN_REGISTER_MODE</a> value that specifies the current network registration mode of the device.  The value is meaningful only if the method returns <b>S_OK</b>.


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
The registration mode is not available.  The Mobile Broadband service is currently probing the device for the information.  When the registration mode is available, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/5c916f16-e8f5-4c8a-942c-3a9ae11905a7">OnRegisterModeAvailable</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>	E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the register mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>
 




## -remarks



See <a href="https://msdn.microsoft.com/be64aa55-5a31-4909-9f34-634f7b14fc30">MBN_REGISTER_MODE</a> for details on possible registration modes.

For recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the  error condition is over (when a PIN is entered). Then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/5c916f16-e8f5-4c8a-942c-3a9ae11905a7">OnRegisterModeAvailable</a> method of   <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a>
 

 

