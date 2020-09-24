---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsDeleteComplete
title: IMbnSmsEvents::OnSmsDeleteComplete (mbnapi.h)
description: Notification method that signals the completion of an SMS deletion operation.
helpviewer_keywords: ["E_MBN_BAD_SIM","E_MBN_PIN_REQUIRED","E_MBN_SIM_NOT_INSERTED","E_MBN_SMS_FILTER_NOT_SUPPORTED","E_MBN_SMS_INVALID_MEMORY_INDEX","E_MBN_SMS_MEMORY_FAILURE","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnSmsEvents interface [Microsoft Broadband Networks]","OnSmsDeleteComplete method","IMbnSmsEvents.OnSmsDeleteComplete","IMbnSmsEvents::OnSmsDeleteComplete","OnSmsDeleteComplete","OnSmsDeleteComplete method [Microsoft Broadband Networks]","OnSmsDeleteComplete method [Microsoft Broadband Networks]","IMbnSmsEvents interface","S_OK","mbn.imbnsmsevents_onsmsdeletecomplete","mbnapi/IMbnSmsEvents::OnSmsDeleteComplete"]
old-location: mbn\imbnsmsevents_onsmsdeletecomplete.htm
tech.root: mbn
ms.assetid: bac1c7b3-fedc-47fb-822c-712805a86f6e
ms.date: 12/05/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, E_MBN_SMS_FILTER_NOT_SUPPORTED, E_MBN_SMS_INVALID_MEMORY_INDEX, E_MBN_SMS_MEMORY_FAILURE, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsDeleteComplete method, IMbnSmsEvents.OnSmsDeleteComplete, IMbnSmsEvents::OnSmsDeleteComplete, OnSmsDeleteComplete, OnSmsDeleteComplete method [Microsoft Broadband Networks], OnSmsDeleteComplete method [Microsoft Broadband Networks],IMbnSmsEvents interface, S_OK, mbn.imbnsmsevents_onsmsdeletecomplete, mbnapi/IMbnSmsEvents::OnSmsDeleteComplete
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
 - IMbnSmsEvents::OnSmsDeleteComplete
 - mbnapi/IMbnSmsEvents::OnSmsDeleteComplete
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
 - IMbnSmsEvents.OnSmsDeleteComplete
---

# IMbnSmsEvents::OnSmsDeleteComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that signals the completion of an SMS deletion operation.

## -parameters

### -param sms [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface representing the Mobile Broadband device from which the messages were deleted.

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
Either the SMS operation or the particular SMS format is not supported by the device.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_MEMORY_FAILURE"></a><a id="e_mbn_sms_memory_failure"></a><dl>
<dt><b>E_MBN_SMS_MEMORY_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
SMS memory failure.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_INVALID_MEMORY_INDEX"></a><a id="e_mbn_sms_invalid_memory_index"></a><dl>
<dt><b>E_MBN_SMS_INVALID_MEMORY_INDEX</b></dt>
</dl>
</td>
<td width="60%">
There is no memory index with the requested value.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_FILTER_NOT_SUPPORTED"></a><a id="e_mbn_sms_filter_not_supported"></a><dl>
<dt><b>E_MBN_SMS_FILTER_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support the requested filter.  	

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>