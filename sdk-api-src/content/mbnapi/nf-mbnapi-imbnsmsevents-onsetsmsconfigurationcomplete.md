---
UID: NF:mbnapi.IMbnSmsEvents.OnSetSmsConfigurationComplete
title: IMbnSmsEvents::OnSetSmsConfigurationComplete (mbnapi.h)
description: Notification method signaling that a set SMS configuration operation has completed, or that the SMS subsystem is initialized and ready for operation.
helpviewer_keywords: ["E_MBN_BAD_SIM","E_MBN_PIN_REQUIRED","E_MBN_SIM_NOT_INSERTED","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnSmsEvents interface [Microsoft Broadband Networks]","OnSetSmsConfigurationComplete method","IMbnSmsEvents.OnSetSmsConfigurationComplete","IMbnSmsEvents::OnSetSmsConfigurationComplete","OnSetSmsConfigurationComplete","OnSetSmsConfigurationComplete method [Microsoft Broadband Networks]","OnSetSmsConfigurationComplete method [Microsoft Broadband Networks]","IMbnSmsEvents interface","S_OK","mbn.imbnsmsevents_onsetsmsconfigurationcomplete","mbnapi/IMbnSmsEvents::OnSetSmsConfigurationComplete"]
old-location: mbn\imbnsmsevents_onsetsmsconfigurationcomplete.htm
tech.root: mbn
ms.assetid: d5e5b1fc-88c3-4438-a160-f9969ed6d91a
ms.date: 12/05/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnSmsEvents interface [Microsoft Broadband Networks],OnSetSmsConfigurationComplete method, IMbnSmsEvents.OnSetSmsConfigurationComplete, IMbnSmsEvents::OnSetSmsConfigurationComplete, OnSetSmsConfigurationComplete, OnSetSmsConfigurationComplete method [Microsoft Broadband Networks], OnSetSmsConfigurationComplete method [Microsoft Broadband Networks],IMbnSmsEvents interface, S_OK, mbn.imbnsmsevents_onsetsmsconfigurationcomplete, mbnapi/IMbnSmsEvents::OnSetSmsConfigurationComplete
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnSmsEvents::OnSetSmsConfigurationComplete
 - mbnapi/IMbnSmsEvents::OnSetSmsConfigurationComplete
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
 - IMbnSmsEvents.OnSetSmsConfigurationComplete
---

# IMbnSmsEvents::OnSetSmsConfigurationComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method signaling that a set SMS configuration operation has completed, or that the SMS subsystem is initialized and ready for operation.

## -parameters

### -param sms [in]

A pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface representing the Mobile Broadband device for which the SMS configuration has been updated.

### -param requestID [in]

A request ID assigned by the Mobile Broadband service to identify the operation.

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
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.  	

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The SMS format is not supported by the device.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

This method is used to notify an application of the completion of a set SMS configuration operation. The application can use the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface to get the new configuration information. It is also used by the device to indicate the readiness of the device's SMS subsystem. Upon system startup or device insertion, this method will be called to notify applications that the device SMS subsystem is ready for operation.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>