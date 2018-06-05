---
UID: NF:mbnapi.IMbnServiceActivationEvents.OnActivationComplete
title: IMbnServiceActivationEvents::OnActivationComplete
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that a service activation request ahs completed.
old-location: mbn\imbnserviceactivationevents_onactivationcomplete.htm
old-project: mbn
ms.assetid: bc1c85b3-1b7b-4439-9358-801da8f4c79b
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: E_INVALIDARG, E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_PROVIDER_NOT_VISIBLE, E_MBN_RADIO_POWER_OFF, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnServiceActivationEvents interface [Microsoft Broadband Networks],OnActivationComplete method, IMbnServiceActivationEvents.OnActivationComplete, IMbnServiceActivationEvents::OnActivationComplete, OnActivationComplete, OnActivationComplete method [Microsoft Broadband Networks], OnActivationComplete method [Microsoft Broadband Networks],IMbnServiceActivationEvents interface, S_OK, mbn.imbnserviceactivationevents_onactivationcomplete, mbnapi/IMbnServiceActivationEvents::OnActivationComplete
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
-	IMbnServiceActivationEvents.OnActivationComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnServiceActivationEvents::OnActivationComplete


## -description


Notification method called by the Mobile Broadband service to indicate that a service activation request ahs completed.


## -parameters




### -param serviceActivation [in]

Pointer to an <a href="https://msdn.microsoft.com/cf23be24-f7a8-41b9-81f1-c267a265f85b">IMbnServiceActivation</a> interface representing the device on which the request was performed.


### -param vendorSpecificData [in]

A byte array containing the data returned by the underlying Mobile Broadband miniport driver in <a href="https://msdn.microsoft.com/library/windows/hardware/ff567858">NDIS_STATUS_WWAN_SERVICE_ACTIVATION</a>.


### -param requestID [in]

The request ID assigned by the Mobile Broadband service when the request was initialized.


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
<td width="40%"><a id="E_INVALIDARG"></a><a id="e_invalidarg"></a><dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The miniport driver detected incorrect input data in the request.

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
<td width="40%"><a id="E_MBN_RADIO_POWER_OFF"></a><a id="e_mbn_radio_power_off"></a><dl>
<dt><b>E_MBN_RADIO_POWER_OFF</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband device is not powered up.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PROVIDER_NOT_VISIBLE"></a><a id="e_mbn_provider_not_visible"></a><dl>
<dt><b>E_MBN_PROVIDER_NOT_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
The service provider is not visible.

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
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this operation.

</td>
</tr>
</table>
 


### -param networkError [in]

The error code returned by the network during the activation operation. This value is meaningful only when <i>status</i> is not S_OK. 

The exact value of <i>networkError</i> is driver/network dependent.


## -returns



This method must return <b>S_OK</b>.




## -remarks



Successful service activation will also result in a change to the  ready state of the device. the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/eb4364b8-cbbf-44c7-ae13-66950ce614e9">OnReadyStateChange</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a> as notification.




## -see-also




<a href="https://msdn.microsoft.com/b3385523-f1ab-403d-9244-7683a7e9f95a">IMbnServiceActivationEvents</a>
 

 

