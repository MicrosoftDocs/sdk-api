---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsSendComplete
title: IMbnSmsEvents::OnSmsSendComplete
author: windows-sdk-content
description: Notification method that indicates the completion of a message send operation.
old-location: mbn\imbnsmsevents_onsmssendcomplete.htm
old-project: mbn
ms.assetid: 4c08b173-7e9e-4b4f-8068-1a90c57eea90
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: E_INVALIDARG, E_MBN_BAD_SIM, E_MBN_NOT_REGISTERED, E_MBN_PIN_REQUIRED, E_MBN_SERVICE_NOT_ACTIVATED, E_MBN_SIM_NOT_INSERTED, E_MBN_SMS_ENCODING_NOT_SUPPORTED, E_MBN_SMS_LANG_NOT_SUPPORTED, E_MBN_SMS_MEMORY_FAILURE, E_MBN_SMS_MEMORY_FULL, E_MBN_SMS_NETWORK_TIMEOUT, E_MBN_SMS_OPERATION_NOT_ALLOWED, E_MBN_SMS_UNKNOWN_SMSC_ADDRESS, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsSendComplete method, IMbnSmsEvents.OnSmsSendComplete, IMbnSmsEvents::OnSmsSendComplete, OnSmsSendComplete, OnSmsSendComplete method [Microsoft Broadband Networks], OnSmsSendComplete method [Microsoft Broadband Networks],IMbnSmsEvents interface, S_OK, mbn.imbnsmsevents_onsmssendcomplete, mbnapi/IMbnSmsEvents::OnSmsSendComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsEvents.OnSmsSendComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsEvents::OnSmsSendComplete


## -description


Notification method that indicates the completion of a message send operation.


## -parameters




### -param sms [in]

An <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface representing the Mobile Broadband device from which the operation completed.


### -param requestID [in]

A  request ID assigned by the Mobile Broadband service to identify the operation.


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
<td width="40%"><a id="E_MBN_SMS_UNKNOWN_SMSC_ADDRESS"></a><a id="e_mbn_sms_unknown_smsc_address"></a><dl>
<dt><b>E_MBN_SMS_UNKNOWN_SMSC_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Unknown or incomplete SMS service center address.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SERVICE_NOT_ACTIVATED"></a><a id="e_mbn_service_not_activated"></a><dl>
<dt><b>E_MBN_SERVICE_NOT_ACTIVATED</b></dt>
</dl>
</td>
<td width="60%">
Cellular service is not activated on the device.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_INVALIDARG"></a><a id="e_invalidarg"></a><dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The device detected invalid parameters in the send request.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_NETWORK_TIMEOUT"></a><a id="e_mbn_sms_network_timeout"></a><dl>
<dt><b>E_MBN_SMS_NETWORK_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
There was a network timeout.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_NOT_REGISTERED"></a><a id="e_mbn_not_registered"></a><dl>
<dt><b>E_MBN_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The device is not registered to any network.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_LANG_NOT_SUPPORTED"></a><a id="e_mbn_sms_lang_not_supported"></a><dl>
<dt><b>E_MBN_SMS_LANG_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The CDMA device does not support the language.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_ENCODING_NOT_SUPPORTED"></a><a id="e_mbn_sms_encoding_not_supported"></a><dl>
<dt><b>E_MBN_SMS_ENCODING_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The CDMA device does not support the requested encoding.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_OPERATION_NOT_ALLOWED"></a><a id="e_mbn_sms_operation_not_allowed"></a><dl>
<dt><b>E_MBN_SMS_OPERATION_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
The requested SMS operation is not allowed by the SIM.  	

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_SMS_MEMORY_FULL"></a><a id="e_mbn_sms_memory_full"></a><dl>
<dt><b>E_MBN_SMS_MEMORY_FULL</b></dt>
</dl>
</td>
<td width="60%">
The device/SIM memory is full.  	

</td>
</tr>
</table>
 


## -returns



This method must return <b>S_OK</b>.




## -remarks



A send operation should be tried only after the device is successfully registered to the network.




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 

