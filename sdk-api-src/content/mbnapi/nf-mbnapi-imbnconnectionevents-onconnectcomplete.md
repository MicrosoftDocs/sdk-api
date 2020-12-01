---
UID: NF:mbnapi.IMbnConnectionEvents.OnConnectComplete
title: IMbnConnectionEvents::OnConnectComplete (mbnapi.h)
description: Notification method that signals the completion of a connection operation.
helpviewer_keywords: ["E_MBN_ACTIVE_CONNECTION","E_MBN_INVALID_ACCESS_STRING","E_MBN_MAX_ACTIVATED_CONTEXTS","E_MBN_PACKET_SVC_DETACHED","E_MBN_PIN_REQUIRED","E_MBN_PROVIDER_NOT_VISIBLE","E_MBN_RADIO_POWER_OFF","E_MBN_SERVICE_NOT_ACTIVATED","E_MBN_SIM_NOT_INSERTED","E_MBN_VOICE_CALL_IN_PROGRESS","HRESULT_FROM_WIN32(ERROR_INVALID_PASSWORD)","IMbnConnectionEvents interface [Microsoft Broadband Networks]","OnConnectComplete method","IMbnConnectionEvents.OnConnectComplete","IMbnConnectionEvents::OnConnectComplete","OnConnectComplete","OnConnectComplete method [Microsoft Broadband Networks]","OnConnectComplete method [Microsoft Broadband Networks]","IMbnConnectionEvents interface","S_OK","mbn.imbnconnectionevents_onconnectcomplete","mbnapi/IMbnConnectionEvents::OnConnectComplete"]
old-location: mbn\imbnconnectionevents_onconnectcomplete.htm
tech.root: mbn
ms.assetid: d770eda5-43f4-44d3-a870-fc54f9374610
ms.date: 12/05/2018
ms.keywords: E_MBN_ACTIVE_CONNECTION, E_MBN_INVALID_ACCESS_STRING, E_MBN_MAX_ACTIVATED_CONTEXTS, E_MBN_PACKET_SVC_DETACHED, E_MBN_PIN_REQUIRED, E_MBN_PROVIDER_NOT_VISIBLE, E_MBN_RADIO_POWER_OFF, E_MBN_SERVICE_NOT_ACTIVATED, E_MBN_SIM_NOT_INSERTED, E_MBN_VOICE_CALL_IN_PROGRESS, HRESULT_FROM_WIN32(ERROR_INVALID_PASSWORD), IMbnConnectionEvents interface [Microsoft Broadband Networks],OnConnectComplete method, IMbnConnectionEvents.OnConnectComplete, IMbnConnectionEvents::OnConnectComplete, OnConnectComplete, OnConnectComplete method [Microsoft Broadband Networks], OnConnectComplete method [Microsoft Broadband Networks],IMbnConnectionEvents interface, S_OK, mbn.imbnconnectionevents_onconnectcomplete, mbnapi/IMbnConnectionEvents::OnConnectComplete
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
 - IMbnConnectionEvents::OnConnectComplete
 - mbnapi/IMbnConnectionEvents::OnConnectComplete
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
 - IMbnConnectionEvents.OnConnectComplete
---

# IMbnConnectionEvents::OnConnectComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that signals the completion of a connection operation.

## -parameters

### -param newConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the device on which the connection operation has completed.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service to identify the connection operation.

### -param status [in]

The completion status.

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
<td width="40%"><a id="E_MBN_SIM_NOT_INSERTED"></a><a id="e_mbn_sim_not_inserted"></a><dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
There is no SIM in the device.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SERVICE_NOT_ACTIVATED"></a><a id="e_mbn_service_not_activated"></a><dl>
<dt><b>E_MBN_SERVICE_NOT_ACTIVATED</b></dt>
</dl>
</td>
<td width="60%">
The network service subscription has expired.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PROVIDER_NOT_VISIBLE"></a><a id="e_mbn_provider_not_visible"></a><dl>
<dt><b>E_MBN_PROVIDER_NOT_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
The provider is not visible.  This applies only to manual registration mode.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_INVALID_ACCESS_STRING"></a><a id="e_mbn_invalid_access_string"></a><dl>
<dt><b>E_MBN_INVALID_ACCESS_STRING</b></dt>
</dl>
</td>
<td width="60%">
The connection access string is not correct.

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_INVALID_PASSWORD_"></a><a id="hresult_from_win32_error_invalid_password_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_PASSWORD)</b></dt>
</dl>
</td>
<td width="60%">
The name or password using in the connection profile is not correct.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_VOICE_CALL_IN_PROGRESS"></a><a id="e_mbn_voice_call_in_progress"></a><dl>
<dt><b>E_MBN_VOICE_CALL_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
An active voice call is in progress.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_MAX_ACTIVATED_CONTEXTS"></a><a id="e_mbn_max_activated_contexts"></a><dl>
<dt><b>E_MBN_MAX_ACTIVATED_CONTEXTS</b></dt>
</dl>
</td>
<td width="60%">
There is already an Mobile Broadband context active.  The Mobile Broadband service does not currently support multiple active contexts.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_RADIO_POWER_OFF"></a><a id="e_mbn_radio_power_off"></a><dl>
<dt><b>E_MBN_RADIO_POWER_OFF</b></dt>
</dl>
</td>
<td width="60%">
The device radio is off.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PACKET_SVC_DETACHED"></a><a id="e_mbn_packet_svc_detached"></a><dl>
<dt><b>E_MBN_PACKET_SVC_DETACHED</b></dt>
</dl>
</td>
<td width="60%">
No active attached packet service is available.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_ACTIVE_CONNECTION"></a><a id="e_mbn_active_connection"></a><dl>
<dt><b>E_MBN_ACTIVE_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The device is already connected to the network.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

Once an activation context is established, an application can use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> to get the current connection state.  

When the connection operation results in an error, an application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-getactivationnetworkerror">GetActivationNetworkError</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface to obtain network error information.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>