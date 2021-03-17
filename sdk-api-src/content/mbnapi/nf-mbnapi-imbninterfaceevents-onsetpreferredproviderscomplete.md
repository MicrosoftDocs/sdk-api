---
UID: NF:mbnapi.IMbnInterfaceEvents.OnSetPreferredProvidersComplete
title: IMbnInterfaceEvents::OnSetPreferredProvidersComplete (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetPreferredProviders operation.
helpviewer_keywords: ["E_MBN_BAD_SIM","E_MBN_PIN_REQUIRED","E_MBN_SIM_NOT_INSERTED","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnSetPreferredProvidersComplete method","IMbnInterfaceEvents.OnSetPreferredProvidersComplete","IMbnInterfaceEvents::OnSetPreferredProvidersComplete","OnSetPreferredProvidersComplete","OnSetPreferredProvidersComplete method [Microsoft Broadband Networks]","OnSetPreferredProvidersComplete method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","S_OK","mbn.imbninterfaceevents_onsetpreferredproviderscomplete","mbnapi/IMbnInterfaceEvents::OnSetPreferredProvidersComplete"]
old-location: mbn\imbninterfaceevents_onsetpreferredproviderscomplete.htm
tech.root: mbn
ms.assetid: 9cd5d185-ff0f-45f4-91fc-da601d256914
ms.date: 12/05/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnSetPreferredProvidersComplete method, IMbnInterfaceEvents.OnSetPreferredProvidersComplete, IMbnInterfaceEvents::OnSetPreferredProvidersComplete, OnSetPreferredProvidersComplete, OnSetPreferredProvidersComplete method [Microsoft Broadband Networks], OnSetPreferredProvidersComplete method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, S_OK, mbn.imbninterfaceevents_onsetpreferredproviderscomplete, mbnapi/IMbnInterfaceEvents::OnSetPreferredProvidersComplete
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
 - IMbnInterfaceEvents::OnSetPreferredProvidersComplete
 - mbnapi/IMbnInterfaceEvents::OnSetPreferredProvidersComplete
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
 - IMbnInterfaceEvents.OnSetPreferredProvidersComplete
---

# IMbnInterfaceEvents::OnSetPreferredProvidersComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-setpreferredproviders">SetPreferredProviders</a> operation.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents a device on which this operation was performed.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service for this asynchronous operation.

### -param status [in]

The operation completion status.

The following table lists the valid values for this status.

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
The operation  was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The device requires a PIN to be entered for this operation to complete.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SIM_NOT_INSERTED"></a><a id="e_mbn_sim_not_inserted"></a><dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
The SIM is not inserted.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_BAD_SIM"></a><a id="e_mbn_bad_sim"></a><dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

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
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

If the operation completed successfully, that is, when <i>status</i> is  <b>S_OK</b>, then the application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getpreferredproviders">GetPreferredProviders</a> method of the  passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get an updated list of preferred providers.

If multiple applications registered for notifications, then this method will be called on all registered applications. This means that an application that did not initiate the update operation will also receive a notification.

If a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-setpreferredproviders">SetPreferredProviders</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> results in a change in the preferred provider list, then the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onpreferredproviderschange">OnPreferredProvidersChange</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a> will not be called.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>