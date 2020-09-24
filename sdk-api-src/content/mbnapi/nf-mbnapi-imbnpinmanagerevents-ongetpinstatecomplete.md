---
UID: NF:mbnapi.IMbnPinManagerEvents.OnGetPinStateComplete
title: IMbnPinManagerEvents::OnGetPinStateComplete (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate the completion of an asynchronous operation triggered by a call to the GetPinState method of IMbnPinManager.
helpviewer_keywords: ["E_MBN_BAD_SIM","E_MBN_SIM_NOT_INSERTED","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnPinManagerEvents interface [Microsoft Broadband Networks]","OnGetPinStateComplete method","IMbnPinManagerEvents.OnGetPinStateComplete","IMbnPinManagerEvents::OnGetPinStateComplete","OnGetPinStateComplete","OnGetPinStateComplete method [Microsoft Broadband Networks]","OnGetPinStateComplete method [Microsoft Broadband Networks]","IMbnPinManagerEvents interface","S_OK","mbn.imbnpinmanagerevents_ongetpinstatecomplete","mbnapi/IMbnPinManagerEvents::OnGetPinStateComplete"]
old-location: mbn\imbnpinmanagerevents_ongetpinstatecomplete.htm
tech.root: mbn
ms.assetid: e228073b-896a-4d2d-a8a5-f8fa7a52ffc2
ms.date: 12/05/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnPinManagerEvents interface [Microsoft Broadband Networks],OnGetPinStateComplete method, IMbnPinManagerEvents.OnGetPinStateComplete, IMbnPinManagerEvents::OnGetPinStateComplete, OnGetPinStateComplete, OnGetPinStateComplete method [Microsoft Broadband Networks], OnGetPinStateComplete method [Microsoft Broadband Networks],IMbnPinManagerEvents interface, S_OK, mbn.imbnpinmanagerevents_ongetpinstatecomplete, mbnapi/IMbnPinManagerEvents::OnGetPinStateComplete
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
 - IMbnPinManagerEvents::OnGetPinStateComplete
 - mbnapi/IMbnPinManagerEvents::OnGetPinStateComplete
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
 - IMbnPinManagerEvents.OnGetPinStateComplete
---

# IMbnPinManagerEvents::OnGetPinStateComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate the completion of an asynchronous operation triggered by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>.

## -parameters

### -param pinManager [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface that represents the Mobile Broadband device for which the operation was performed.

### -param pinInfo [in]

A <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info">MBN_PIN_INFO</a> structure that contains the device PIN information.

If <b>pinInfo.pinState</b> is set to <b>MBN_PIN_STATE_NONE</b> then no PIN is expected to be entered by device.

If <b>pinInfo.pinState</b> is set to <b>MBN_PIN_STATE_ENTER</b> then the device is expecting a PIN to be entered and <b>pinInfo.pinType</b> represents the type of PIN expected by device.

If <b>pinInfo.pinState</b> is set to <b>MBN_PIN_STATE_UNBLOCK</b> then the device is PIN blocked and a PIN unblock operation should be tried to unblock the device. In this case, <b>pinInfo.pinType</b> represents the PIN type on which the unblock operation should be performed. 


If <b>pinInfo.pinState</b> is set to <b>MBN_PIN_STATE_ENTER</b> or <b>MBN_PIN_STATE_UNBLOCK</b>, then <b>pinInfo.attemptsRemaining</b> contains the number of attempts remaining to enter a valid PIN or PIN unblock key (PUK). If the number of attempts remaining is unknown then <b>pinInfo.attemptsRemaining</b> is set to <b>MBN_ATTEMPTS_REMAINING_UNKNOWN</b>.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service to identify this operation.

### -param status [in]

The operation completion status.

A calling application can expect one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support PIN operations.

</td>
</tr>
<tr>
<td width="40%"><a id="_E_MBN_SIM_NOT_INSERTED"></a><a id="_e_mbn_sim_not_inserted"></a><dl>
<dt><b>	E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
The operation could not complete because a SIM is not in the device.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_BAD_SIM"></a><a id="e_mbn_bad_sim"></a><dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
The operation could not complete because a bad SIM was detected in the device.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

This method is called by the Mobile Broadband service to notify an application of the  completion of an asynchronous operation triggered by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>.    
On successful completion, <i>pinInfo</i> contains information about PIN next expected by the device.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>