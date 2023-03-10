---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.RegisterEndpointNotificationCallback
title: IMMDeviceEnumerator::RegisterEndpointNotificationCallback (mmdeviceapi.h)
description: The RegisterEndpointNotificationCallback method registers a client's notification callback interface.
helpviewer_keywords: ["IMMDeviceEnumerator interface [Core Audio]","RegisterEndpointNotificationCallback method","IMMDeviceEnumerator.RegisterEndpointNotificationCallback","IMMDeviceEnumerator::RegisterEndpointNotificationCallback","IMMDeviceEnumeratorRegisterEndpointNotificationCal","RegisterEndpointNotificationCallback","RegisterEndpointNotificationCallback method [Core Audio]","RegisterEndpointNotificationCallback method [Core Audio]","IMMDeviceEnumerator interface","coreaudio.immdeviceenumerator_registerendpointnotificationcallback","mmdeviceapi/IMMDeviceEnumerator::RegisterEndpointNotificationCallback"]
old-location: coreaudio\immdeviceenumerator_registerendpointnotificationcallback.htm
tech.root: CoreAudio
ms.assetid: 2c524f64-0b35-4433-9768-582dcb580a74
ms.date: 12/05/2018
ms.keywords: IMMDeviceEnumerator interface [Core Audio],RegisterEndpointNotificationCallback method, IMMDeviceEnumerator.RegisterEndpointNotificationCallback, IMMDeviceEnumerator::RegisterEndpointNotificationCallback, IMMDeviceEnumeratorRegisterEndpointNotificationCal, RegisterEndpointNotificationCallback, RegisterEndpointNotificationCallback method [Core Audio], RegisterEndpointNotificationCallback method [Core Audio],IMMDeviceEnumerator interface, coreaudio.immdeviceenumerator_registerendpointnotificationcallback, mmdeviceapi/IMMDeviceEnumerator::RegisterEndpointNotificationCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMMDeviceEnumerator::RegisterEndpointNotificationCallback
 - mmdeviceapi/IMMDeviceEnumerator::RegisterEndpointNotificationCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDeviceEnumerator.RegisterEndpointNotificationCallback
---

# IMMDeviceEnumerator::RegisterEndpointNotificationCallback


## -description

The <b>RegisterEndpointNotificationCallback</b> method registers a client's notification callback interface.

## -parameters

### -param pClient [in]

Pointer to the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient</a> interface that the client is registering for notification callbacks.

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

When notifications are no longer needed, the client can call the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a> method to terminate the notifications.

The client must ensure that the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient</a> object is not released after the <b>RegisterEndpointNotificationCallback</b> call and before calling <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">UnregisterEndpointNotificationCallback</a>. These methods do not call the client's <b>IMMNotificationClient::AddRef</b> and <b>IMMNotificationClient::Release</b> implementations. The client is responsible for maintaining the reference count of the <b>IMMNotificationClient</b> object. The client must increment the count if the <b>RegisterEndpointNotificationCallback</b> call succeeds and release the final reference only after calling <b>UnregisterEndpointNotificationCallback</b> or implement some other mechanism to ensure that the object is not deleted before <b>UnregisterEndpointNotificationCallback</b> is called. Otherwise, the application leaks the resources held by the <b>IMMNotificationClient</b> and any other object that is implemented in the same container. 



For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>