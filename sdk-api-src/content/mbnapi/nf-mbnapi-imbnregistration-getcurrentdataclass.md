---
UID: NF:mbnapi.IMbnRegistration.GetCurrentDataClass
title: IMbnRegistration::GetCurrentDataClass
author: windows-sdk-content
description: Gets the current data class in the current network.
old-location: mbn\imbnregistration_getcurrentdataclass.htm
tech.root: mbn
ms.assetid: 365458a4-74df-4283-94db-3d855acadffe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCurrentDataClass, GetCurrentDataClass method [Microsoft Broadband Networks], GetCurrentDataClass method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetCurrentDataClass method, IMbnRegistration.GetCurrentDataClass, IMbnRegistration::GetCurrentDataClass, mbn.imbnregistration_getcurrentdataclass, mbnapi/IMbnRegistration::GetCurrentDataClass
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMbnRegistration.GetCurrentDataClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnRegistration::GetCurrentDataClass


## -description


Gets the current data class in the current network.


## -parameters




### -param currentDataClass [out]

A pointer to a  <a href="https://msdn.microsoft.com/798d5d72-9267-433f-b890-9302a0a600f2">MBN_DATA_CLASS</a> value.  This parameter is meaningful only if the function returns <b>S_OK</b>.


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
The data classes are not available.  the Mobile Broadband service is currently probing the device for the information.  When the data classes are available, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/19199009-a4ac-4bf9-adfc-46c06d861485">OnPacketServiceStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the data classes.

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



The <b>GetCurrentDataClass</b> method returns the data class in the current network. This value can be set to <b>MBN_DATA_CLASS_NONE</b> if value is not known.

The current data class can change automatically as a device moves from one cellular network to another. Whenever such a change occurs, the Mobile Broadband service will notify applications by calling the <a href="https://msdn.microsoft.com/19199009-a4ac-4bf9-adfc-46c06d861485">OnPacketServiceStateChange</a> method of  <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered). Afterwards, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/19199009-a4ac-4bf9-adfc-46c06d861485">OnPacketServiceStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a>
 

 

