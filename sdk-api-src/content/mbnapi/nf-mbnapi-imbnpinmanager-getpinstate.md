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

# IMbnPinManager::GetPinState


## -description


Gets the current PIN state of the device.


## -parameters




### -param requestID [out]

A pointer to the  request ID set by the Mobile Broadband service for this asynchronous request.  The response will contain the same request ID.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
</table>
 




## -remarks



The <b>GetPinState</b> method initiates an asynchronous request for the PIN state of the device. The PIN state indicates if a PIN needs to be entered for a requested operation to complete. It also contains information about which type of PIN is expected by a device and optionally it provides the number of attempts remaining for entering a valid PIN.

This method always returns the current PIN state of the device. It does not cache the PIN state at the time when this object is created.  Instead it always contacts the device and returns the current PIN state of the device.

Since this is an asynchronous operation, <b>GetPinState</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the   <a href="https://msdn.microsoft.com/e228073b-896a-4d2d-a8a5-f8fa7a52ffc2">OnGetPinStateComplete</a> method of  <a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>.

Whenever an operation returns <b>E_MBN_PIN_REQUIRED</b> or the ready state reported by the device is <b>MBN_READY_STATE_DEVICE_LOCKED</b>, an application should use this method to query the type of PIN required to unlock the device or SIM.

While this operation is in progress,  if the Mobile Broadband device gets removed from the system then a call to the   <a href="https://msdn.microsoft.com/e228073b-896a-4d2d-a8a5-f8fa7a52ffc2">OnGetPinStateComplete</a> method of  <a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a> is not guaranteed.





## -see-also




<a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a>
 

 

