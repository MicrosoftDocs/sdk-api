---
UID: NF:mbnapi.IMbnPinManager.GetPinState
title: IMbnPinManager::GetPinState (mbnapi.h)
description: Gets the current PIN state of the device.
helpviewer_keywords: ["GetPinState","GetPinState method [Microsoft Broadband Networks]","GetPinState method [Microsoft Broadband Networks]","IMbnPinManager interface","IMbnPinManager interface [Microsoft Broadband Networks]","GetPinState method","IMbnPinManager.GetPinState","IMbnPinManager::GetPinState","mbn.imbnpinmanager_getpinstate","mbnapi/IMbnPinManager::GetPinState"]
old-location: mbn\imbnpinmanager_getpinstate.htm
tech.root: mbn
ms.assetid: 34378403-cf58-4ada-9eb6-f5dad5f69bc9
ms.date: 12/05/2018
ms.keywords: GetPinState, GetPinState method [Microsoft Broadband Networks], GetPinState method [Microsoft Broadband Networks],IMbnPinManager interface, IMbnPinManager interface [Microsoft Broadband Networks],GetPinState method, IMbnPinManager.GetPinState, IMbnPinManager::GetPinState, mbn.imbnpinmanager_getpinstate, mbnapi/IMbnPinManager::GetPinState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnPinManager::GetPinState
 - mbnapi/IMbnPinManager::GetPinState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPinManager.GetPinState
---

# IMbnPinManager::GetPinState


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

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

Since this is an asynchronous operation, <b>GetPinState</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the   <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-ongetpinstatecomplete">OnGetPinStateComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>.

Whenever an operation returns <b>E_MBN_PIN_REQUIRED</b> or the ready state reported by the device is <b>MBN_READY_STATE_DEVICE_LOCKED</b>, an application should use this method to query the type of PIN required to unlock the device or SIM.

While this operation is in progress,  if the Mobile Broadband device gets removed from the system then a call to the   <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-ongetpinstatecomplete">OnGetPinStateComplete</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a> is not guaranteed.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>