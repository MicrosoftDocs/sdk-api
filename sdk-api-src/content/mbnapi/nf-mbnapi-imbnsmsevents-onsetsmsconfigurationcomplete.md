---
UID: NF:mbnapi.IMbnSmsEvents.OnSetSmsConfigurationComplete
title: IMbnSmsEvents::OnSetSmsConfigurationComplete
author: windows-sdk-content
description: Notification method signaling that a set SMS configuration operation has completed, or that the SMS subsystem is initialized and ready for operation.
old-location: mbn\imbnsmsevents_onsetsmsconfigurationcomplete.htm
old-project: mbn
ms.assetid: d5e5b1fc-88c3-4438-a160-f9969ed6d91a
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnSmsEvents interface [Microsoft Broadband Networks],OnSetSmsConfigurationComplete method, IMbnSmsEvents.OnSetSmsConfigurationComplete, IMbnSmsEvents::OnSetSmsConfigurationComplete, OnSetSmsConfigurationComplete, OnSetSmsConfigurationComplete method [Microsoft Broadband Networks], OnSetSmsConfigurationComplete method [Microsoft Broadband Networks],IMbnSmsEvents interface, S_OK, mbn.imbnsmsevents_onsetsmsconfigurationcomplete, mbnapi/IMbnSmsEvents::OnSetSmsConfigurationComplete
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsEvents.OnSetSmsConfigurationComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsEvents::OnSetSmsConfigurationComplete


## -description


Notification method signaling that a set SMS configuration operation has completed, or that the SMS subsystem is initialized and ready for operation.


## -parameters




### -param sms [in]

A pointer to an <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface representing the Mobile Broadband device for which the SMS configuration has been updated.


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



This method is used to notify an application of the completion of a set SMS configuration operation. The application can use the passed <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface to get the new configuration information. It is also used by the device to indicate the readiness of the device's SMS subsystem. Upon system startup or device insertion, this method will be called to notify applications that the device SMS subsystem is ready for operation.




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 

