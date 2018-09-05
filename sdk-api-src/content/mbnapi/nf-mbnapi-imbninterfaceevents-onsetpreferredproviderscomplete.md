---
UID: NF:mbnapi.IMbnInterfaceEvents.OnSetPreferredProvidersComplete
title: IMbnInterfaceEvents::OnSetPreferredProvidersComplete
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetPreferredProviders operation.
old-location: mbn\imbninterfaceevents_onsetpreferredproviderscomplete.htm
old-project: mbn
ms.assetid: 9cd5d185-ff0f-45f4-91fc-da601d256914
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: E_MBN_BAD_SIM, E_MBN_PIN_REQUIRED, E_MBN_SIM_NOT_INSERTED, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnSetPreferredProvidersComplete method, IMbnInterfaceEvents.OnSetPreferredProvidersComplete, IMbnInterfaceEvents::OnSetPreferredProvidersComplete, OnSetPreferredProvidersComplete, OnSetPreferredProvidersComplete method [Microsoft Broadband Networks], OnSetPreferredProvidersComplete method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, S_OK, mbn.imbninterfaceevents_onsetpreferredproviderscomplete, mbnapi/IMbnInterfaceEvents::OnSetPreferredProvidersComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterfaceEvents.OnSetPreferredProvidersComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents::OnSetPreferredProvidersComplete


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/2ea95b4a-07d9-40d6-bb82-091b49c965c4">SetPreferredProviders</a> operation.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents a device on which this operation was performed.


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



If the operation completed successfully, that is, when <i>status</i> is  <b>S_OK</b>, then the application can call the <a href="https://msdn.microsoft.com/cbd37f0a-4245-415d-bd74-501aa4c7ade7">GetPreferredProviders</a> method of the  passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get an updated list of preferred providers.

If multiple applications registered for notifications, then this method will be called on all registered applications. This means that an application that did not initiate the update operation will also receive a notification.

If a call to the <a href="https://msdn.microsoft.com/2ea95b4a-07d9-40d6-bb82-091b49c965c4">SetPreferredProviders</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> results in a change in the preferred provider list, then the <a href="https://msdn.microsoft.com/ccede3de-4dfd-469f-afb4-d1424c56c7bc">OnPreferredProvidersChange</a> method of  <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a> will not be called.




## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

