---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMbnConnection::GetVoiceCallState


## -description


Gets the voice call state of the device.


## -parameters




### -param voiceCallState [out, retval]

A pointer to a <a href="https://msdn.microsoft.com/1b94b210-e50f-4d7b-a738-9c372364c4f8">MBN_VOICE_CALL_STATE</a> value that specifies the voice call state.  If the method returns anything other than <b>S_OK</b>, the contents of this pointer are not set.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call state not available.  The Mobile Broadband service is probing the device for the information.  The calling application can be notified when the call state is available by registering for the <a href="https://msdn.microsoft.com/c4f243b0-e6d5-4afc-85ad-0f88140c3beb">OnVoiceCallStateChange</a> method of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the call state.

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



For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>,  the Mobile Broadband service will query the device again for this information once the error condition is over. For example, if the device required a PIN to be entered to retrieve the voice call state, then <b>E_MBN_PIN_REQUIRED</b> is returned. After the calling application enters the PIN to unlock the device, the Mobile Broadband service will again try to get the voice call state from the device. The Mobile Broadband service will update the application with the status of a new probe by calling the <a href="https://msdn.microsoft.com/c4f243b0-e6d5-4afc-85ad-0f88140c3beb">OnVoiceCallStateChange</a> method of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

