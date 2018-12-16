---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.RegisterEndpointNotificationCallback
title: IMMDeviceEnumerator::RegisterEndpointNotificationCallback
author: windows-sdk-content
description: The RegisterEndpointNotificationCallback method registers a client's notification callback interface.
old-location: coreaudio\immdeviceenumerator_registerendpointnotificationcallback.htm
tech.root: CoreAudio
ms.assetid: 2c524f64-0b35-4433-9768-582dcb580a74
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMMDeviceEnumerator interface [Core Audio],RegisterEndpointNotificationCallback method, IMMDeviceEnumerator.RegisterEndpointNotificationCallback, IMMDeviceEnumerator::RegisterEndpointNotificationCallback, IMMDeviceEnumeratorRegisterEndpointNotificationCal, RegisterEndpointNotificationCallback, RegisterEndpointNotificationCallback method [Core Audio], RegisterEndpointNotificationCallback method [Core Audio],IMMDeviceEnumerator interface, coreaudio.immdeviceenumerator_registerendpointnotificationcallback, mmdeviceapi/IMMDeviceEnumerator::RegisterEndpointNotificationCallback
ms.topic: method
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmdeviceapi.h
api_name:
 - IMMDeviceEnumerator.RegisterEndpointNotificationCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMDeviceEnumerator::RegisterEndpointNotificationCallback


## -description



The <b>RegisterEndpointNotificationCallback</b> method registers a client's notification callback interface.




## -parameters




### -param pClient [in]

Pointer to the <a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient</a> interface that the client is registering for notification callbacks. 


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



This method registers an IMMNotificationClient interface to be called by the system when the roles, state, existence, or properties of an endpoint device change. The caller implements the IMMNotificationClient interface.

When notifications are no longer needed, the client can call the <a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a> method to terminate the notifications.

The client must ensure that the <a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient</a> object is not released after the <b>RegisterEndpointNotificationCallback</b> call and before calling <a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">UnregisterEndpointNotificationCallback</a>. These methods do not call the client's <b>IMMNotificationClient::AddRef</b> and <b>IMMNotificationClient::Release</b> implementations. The client is responsible for maintaining the reference count of the <b>IMMNotificationClient</b> object. The client must increment the count if the <b>RegisterEndpointNotificationCallback</b> call succeeds and release the final reference only after calling <b>UnregisterEndpointNotificationCallback</b> or implement some other mechanism to ensure that the object is not deleted before <b>UnregisterEndpointNotificationCallback</b> is called. Otherwise, the application leaks the resources held by the <b>IMMNotificationClient</b> and any other object that is implemented in the same container. 



For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.





## -see-also




<a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>



<a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a>



<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

