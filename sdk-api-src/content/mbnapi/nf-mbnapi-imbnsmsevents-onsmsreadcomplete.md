---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsReadComplete
title: IMbnSmsEvents::OnSmsReadComplete
author: windows-sdk-content
description: Notification method indicating the completion of a message read operation.
old-location: mbn\imbnsmsevents_onsmsreadcomplete.htm
tech.root: mbn
ms.assetid: 58478c9d-6df2-466b-85bc-1c571f4429ce
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, E_MBN_SMS_FILTER_NOT_SUPPORTED, E_MBN_SMS_INVALID_MEMORY_INDEX, E_MBN_SMS_MEMORY_FAILURE, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsReadComplete method, IMbnSmsEvents.OnSmsReadComplete, IMbnSmsEvents::OnSmsReadComplete, OnSmsReadComplete, OnSmsReadComplete method [Microsoft Broadband Networks], OnSmsReadComplete method [Microsoft Broadband Networks],IMbnSmsEvents interface, S_OK, mbn.imbnsmsevents_onsmsreadcomplete, mbnapi/IMbnSmsEvents::OnSmsReadComplete
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsEvents.OnSmsReadComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnSmsEvents::OnSmsReadComplete


## -description


Notification method indicating the completion of a message read operation.


## -parameters




### -param sms [in]

An <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface representing the message store that completed the operation.


### -param smsFormat [in]

An <a href="https://msdn.microsoft.com/ece079e2-43a2-4ca9-9aa7-1b9484f0176e">MBN_SMS_FORMAT</a> value that defines the format of the SMS message.


### -param readMsgs [in]

An array of messages read from the device.


### -param moreMsgs [in]

A Boolean value that indicates whether there are more messages still being processed.  If this is <b>TRUE</b>, then <b>OnSmsReadComplete</b> will be called repeatedly until there are not more messages and <i>moreMsgs</i> is <b>FALSE</b>.


### -param requestID [in]

A request ID assigned by the Mobile Broadband service to identify the message read operation.


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




## -remarks



For GSM devices, the calling application should call <a href="_com_IUnknown_QueryInterface">QueryInterface</a> on the each element in <i>readMsgs</i> for an <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface.

  For CDMA devices, if <i>smsFormat</i> is <b>MBN_SMS_FORMAT_TEXT</b>,  the application should call <a href="_com_IUnknown_QueryInterface">QueryInterface</a> for an <a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a> interface; otherwise, if <i>smsFormat</i> is <b>MBN_SMS_FORMAT_PDU</b>, the application should call <b>QueryInterface</b> for an <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface.

If a read request results in a large amount of messages being read, then <b>OnSmsReadComplete</b> may be called repeatedly until <i>moreMsgs</i> indicates there are no more messages to be read. 




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 

