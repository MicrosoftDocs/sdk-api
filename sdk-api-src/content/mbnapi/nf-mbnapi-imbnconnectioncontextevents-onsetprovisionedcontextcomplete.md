---
UID: NF:mbnapi.IMbnConnectionContextEvents.OnSetProvisionedContextComplete
title: IMbnConnectionContextEvents::OnSetProvisionedContextComplete (mbnapi.h)
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that the provisioned context in the device has been set.
old-location: mbn\imbnconnectioncontextevents_onsetprovisionedcontextcomplete.htm
tech.root: mbn
ms.assetid: 06e1071d-c541-4824-9b56-f2d18f41e972
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: E_INVALIDARG, E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), HRESULT_FROM_WIN32(ERROR_WRITE_FAULT), IMbnConnectionContextEvents interface [Microsoft Broadband Networks],OnSetProvisionedContextComplete method, IMbnConnectionContextEvents.OnSetProvisionedContextComplete, IMbnConnectionContextEvents::OnSetProvisionedContextComplete, OnSetProvisionedContextComplete, OnSetProvisionedContextComplete method [Microsoft Broadband Networks], OnSetProvisionedContextComplete method [Microsoft Broadband Networks],IMbnConnectionContextEvents interface, S_OK, mbn.imbnconnectioncontextevents_onsetprovisionedcontextcomplete, mbnapi/IMbnConnectionContextEvents::OnSetProvisionedContextComplete
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
 - IMbnConnectionContextEvents.OnSetProvisionedContextComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionContextEvents::OnSetProvisionedContextComplete


## -description


Notification method called by the Mobile Broadband service to indicate that the  provisioned context in the device has been set.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface that represents the device for which the context has been set.


### -param requestID [in]

A request ID set by the Mobile Broadband service to identify the operation that set the context.


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
<td width="40%"><a id="E_MBN_PIN_REQUIRED"></a><a id="e_mbn_pin_required"></a><dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.

</td>
</tr>
<tr>
<td width="40%"><a id="E_INVALIDARG"></a><a id="e_invalidarg"></a><dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The context ID or provider ID given in the request is not valid.

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
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_WRITE_FAULT_"></a><a id="hresult_from_win32_error_write_fault_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_WRITE_FAULT)</b></dt>
</dl>
</td>
<td width="60%">
An update in either SIM or device memory failed.

</td>
</tr>
</table>
 


## -returns



This method must return <b>S_OK</b>.




## -remarks



A calling application can pass an <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface to <i>newInterface</i> to get the updated list of provisioned contexts in the device.
 However, since this operation is asynchronous, the application must wait for the <a href="https://msdn.microsoft.com/3c8fa150-7c36-4ad8-ada8-2b17693671d9">OnProvisionedContextListChange</a> notification before using this interface to get the contexts.

If there are multiple applications registered to receive notifications then all of them will receive this notification even though only one of them could have initiated this operation.




## -see-also




<a href="https://msdn.microsoft.com/1f73260b-04db-410a-ade0-a835805b2b0a">IMbnConnectionContextEvents</a>
 

 

