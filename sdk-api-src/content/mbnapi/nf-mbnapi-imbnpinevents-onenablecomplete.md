---
UID: NF:mbnapi.IMbnPinEvents.OnEnableComplete
title: IMbnPinEvents::OnEnableComplete (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate that a PIN enable operation has completed.
helpviewer_keywords: ["E_FAIL","E_MBN_BAD_SIM","E_MBN_FAILURE","E_MBN_PIN_REQUIRED","E_MBN_SIM_NOT_INSERTED","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnPinEvents interface [Microsoft Broadband Networks]","OnEnableComplete method","IMbnPinEvents.OnEnableComplete","IMbnPinEvents::OnEnableComplete","OnEnableComplete","OnEnableComplete method [Microsoft Broadband Networks]","OnEnableComplete method [Microsoft Broadband Networks]","IMbnPinEvents interface","S_OK","mbn.imbnpinevents_onenablecomplete","mbnapi/IMbnPinEvents::OnEnableComplete"]
old-location: mbn\imbnpinevents_onenablecomplete.htm
tech.root: mbn
ms.assetid: 577ba161-dbde-4541-8098-72ab682e548b
ms.date: 12/05/2018
ms.keywords: E_FAIL, E_MBN_BAD_SIM, E_MBN_FAILURE, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnPinEvents interface [Microsoft Broadband Networks],OnEnableComplete method, IMbnPinEvents.OnEnableComplete, IMbnPinEvents::OnEnableComplete, OnEnableComplete, OnEnableComplete method [Microsoft Broadband Networks], OnEnableComplete method [Microsoft Broadband Networks],IMbnPinEvents interface, S_OK, mbn.imbnpinevents_onenablecomplete, mbnapi/IMbnPinEvents::OnEnableComplete
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
 - IMbnPinEvents::OnEnableComplete
 - mbnapi/IMbnPinEvents::OnEnableComplete
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
 - IMbnPinEvents.OnEnableComplete
---

# IMbnPinEvents::OnEnableComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate that a PIN enable operation has completed.

## -parameters

### -param pin [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> interface that represents  the PIN type.

### -param pinInfo [in]

A pointer to a <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info">MBN_PIN_INFO</a> structure that contains information on remaining attempts, in case of failure operations.  The contents of <i>pinInfo</i> are meaningful only when <i>status</i> is <b>E_MBN_FAILURE</b>.

### -param requestID [in]

A request ID set by the Mobile Broadband service to identify the PIN enable request.

### -param status [in]

A status code that indicates the outcome of the operation.

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
The operation was  successful.

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this operation.

</td>
</tr>
<tr>
<td width="40%"><a id="E_FAIL"></a><a id="e_fail"></a><dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.  The calling application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> to discover the type of expected PIN.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SIM_NOT_INSERTED"></a><a id="e_mbn_sim_not_inserted"></a><dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
There is no SIM in the device.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_BAD_SIM"></a><a id="e_mbn_bad_sim"></a><dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
There is a bad SIM in the device.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_FAILURE"></a><a id="e_mbn_failure"></a><dl>
<dt><b>E_MBN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
There is a failed attempt to use the PIN.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

The <b>OnEnableComplete</b> method is called by the Mobile Broadband service to report the completion status of a PIN enable operation initialized by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-enable">Enable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>.

The contents of <i>pinInfo</i> are meaningful only when <i>status</i> is <b>E_MBN_FAILURE</b>.  The <b>pinState</b> member should be ignored and <b>pinType</b> field is set to the PIN type of the current <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> interface. This structure contains the attempts remaining to enter a valid PIN. 


For example, if the PIN passed to change a PIN type is incorrect then the operation will fail with a status code of <b>E_MBN_FAILURE</b>. In this case, <b>pinInfo.attemptsRemaining</b> specifies the number of attempts remaining to retry this operation.
If repeated attempts with the wrong PIN causes <b>attemptsRemaining</b> to become 0 then the application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> to get the type of PIN required.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>