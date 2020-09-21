---
UID: NF:mbnapi.IMbnRegistrationEvents.OnSetRegisterModeComplete
title: IMbnRegistrationEvents::OnSetRegisterModeComplete (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate that it has completed a set registration operation.
helpviewer_keywords: ["E_FAIL","E_INVALIDARG","E_MBN_PIN_REQUIRED","E_MBN_PROVIDER_NOT_VISIBLE","E_MBN_SERVICE_NOT_ACTIVATED","HRESULT_FROM_WIN32(ERROR_INVALID_STATE)","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnRegistrationEvents interface [Microsoft Broadband Networks]","OnSetRegisterModeComplete method","IMbnRegistrationEvents.OnSetRegisterModeComplete","IMbnRegistrationEvents::OnSetRegisterModeComplete","OnSetRegisterModeComplete","OnSetRegisterModeComplete method [Microsoft Broadband Networks]","OnSetRegisterModeComplete method [Microsoft Broadband Networks]","IMbnRegistrationEvents interface","S_OK","mbn.imbnregistrationevents_onsetregistermodecomplete","mbnapi/IMbnRegistrationEvents::OnSetRegisterModeComplete"]
old-location: mbn\imbnregistrationevents_onsetregistermodecomplete.htm
tech.root: mbn
ms.assetid: a5ca0776-bd1d-48a0-970a-39c8da69b394
ms.date: 12/05/2018
ms.keywords: E_FAIL, E_INVALIDARG, E_MBN_PIN_REQUIRED, E_MBN_PROVIDER_NOT_VISIBLE, E_MBN_SERVICE_NOT_ACTIVATED, HRESULT_FROM_WIN32(ERROR_INVALID_STATE), HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnSetRegisterModeComplete method, IMbnRegistrationEvents.OnSetRegisterModeComplete, IMbnRegistrationEvents::OnSetRegisterModeComplete, OnSetRegisterModeComplete, OnSetRegisterModeComplete method [Microsoft Broadband Networks], OnSetRegisterModeComplete method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, S_OK, mbn.imbnregistrationevents_onsetregistermodecomplete, mbnapi/IMbnRegistrationEvents::OnSetRegisterModeComplete
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
 - IMbnRegistrationEvents::OnSetRegisterModeComplete
 - mbnapi/IMbnRegistrationEvents::OnSetRegisterModeComplete
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
 - IMbnRegistrationEvents.OnSetRegisterModeComplete
---

# IMbnRegistrationEvents::OnSetRegisterModeComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate that it has completed a set registration operation.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface that represents the applicable device.  The handling application can use this interface to get the current registration state of the device.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service to track the set registration operation.

### -param status [in]

A status code that indicates the outcome of the operation.

A calling application can expect one of the possible values.

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
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_INVALID_STATE_"></a><a id="hresult_from_win32_error_invalid_state_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
There is already an active network connection. The registration mode cannot be changed when there is an already established data connection. The application should first disconnect the connection and then try changing registration mode. If the device is already in the requested mode and connected to requested provider, then the return code will be <b>S_OK</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support the requested registration mode. For example, a CDMA device will return this error when requested to switch to manual registration mode.

</td>
</tr>
<tr>
<td width="40%"><a id="E_FAIL"></a><a id="e_fail"></a><dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed. More information is available in the network error code.

</td>
</tr>
<tr>
<td width="40%"><a id="E_INVALIDARG"></a><a id="e_invalidarg"></a><dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid registration mode input or the provider ID provided as input is longer than maximum length 7 characters or data class provided is invalid.  the Mobile Broadband service will not send the request to the device when invalid arguments are provided in the input.

In manual registration mode, this indicates that the requested provider is forbidden.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is needed for the operation to complete.

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
This occurs only when switching to manual registration mode. The switch is successful but the requested provider is not visible. The device will register to the requested provider when it is visible.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>