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

# BluetoothRegisterForAuthenticationEx function


## -description


The <b>BluetoothRegisterForAuthenticationEx</b> function registers an application for a pin request,  numeric comparison and callback function.
<div class="alert"><b>Note</b>  This API is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters




### -param pbtdiIn

TBD


### -param phRegHandleOut [out]

A pointer to a <b>HBLUETOOTH_AUTHENTICATION_REGISTRATION</b> handle associated with the registered application. Call <a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a> to close
the handle.


### -param pfnCallbackIn [in, optional]

The function that will be called when the authentication event          occurs. This function should match the prototype of <a href="https://msdn.microsoft.com/835a624f-c08d-402c-940b-4443e1b38d58">PFN_AUTHENTICATION_CALLBACK_EX</a>.


### -param pvParam [in, optional]

Optional parameter to be passed through to the callback function specified by <i>pfnCallbackIn</i>.          This parameter  can be anything the application is required to define.


#### - pbtdiln [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure that specifies the bluetooth address to be utilized for comparison.


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
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Win32 Error</b></dt>
</dl>
</td>
<td width="60%">
The registration handle that was provided is invalid.

</td>
</tr>
</table>
 




## -remarks



The caller must provide a valid callback address and must unregister the callback once notification is no longer required.  The deregistration of an authenticated device can be accomplished by calling <a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>.

In scenarios where an application registers for authentication more than once, only the first callback function registered via this function will be called in the application while authentication is in progress.




## -see-also




<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

