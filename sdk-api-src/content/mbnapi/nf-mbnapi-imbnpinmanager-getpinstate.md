---
UID: NF:mbnapi.IMbnPinManager.GetPinState
title: IMbnPinManager::GetPinState
author: windows-sdk-content
description: Gets the current PIN state of the device.
old-location: mbn\imbnpinmanager_getpinstate.htm
old-project: mbn
ms.assetid: 34378403-cf58-4ada-9eb6-f5dad5f69bc9
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GetPinState, GetPinState method [Microsoft Broadband Networks], GetPinState method [Microsoft Broadband Networks],IMbnPinManager interface, IMbnPinManager interface [Microsoft Broadband Networks],GetPinState method, IMbnPinManager.GetPinState, IMbnPinManager::GetPinState, mbn.imbnpinmanager_getpinstate, mbnapi/IMbnPinManager::GetPinState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnPinManager.GetPinState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

