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

# BluetoothSendAuthenticationResponseEx function


## -description


The <b>BluetoothSendAuthenticationResponseEx</b> function is called when an authentication request
to send the passkey or a Numeric Comparison response is made.
<div class="alert"><b>Note</b>  This API is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters




### -param hRadioIn [in, optional]

A handle of the Bluetooth radio device to specify local service information for.


### -param pauthResponse [in]

Pointer to a <a href="https://msdn.microsoft.com/fc7eda84-3e7b-49e9-a1a6-e1759c894e1a">BLUETOOTH_AUTHENTICATE_RESPONSE</a> structure containing the response to the <b>BTH_REMOTE_AUTHENTICATE_REQUEST</b> event.


## -returns



Returns ERROR_SUCCESS upon successful completion; returns the following error codes upon failure:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The device was denied the passkey response. This may also indicate a communications problem with the local radio device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The device returned a failure code during authentication.

</td>
</tr>
</table>
 




## -remarks



Callers can only use this function to respond to a pending authentication request.  Applications should register with <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthenticationEx</a> in order to be notified of incoming authentication requests.  

Only the <b>BLUETOOTH_AUTHENTICATION_METHOD_LEGACY</b>, <b>BLUETOOTH_AUTHENTICATION_METHOD_NUMERIC_COMPARISON</b> and <b>BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY_NOTIFICATION</b> response types are valid.




## -see-also




<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>
 

 

