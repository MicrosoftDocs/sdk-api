---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.UnregisterEndpointNotificationCallback
title: IMMDeviceEnumerator::UnregisterEndpointNotificationCallback (mmdeviceapi.h)
description: The UnregisterEndpointNotificationCallback method deletes the registration of a notification interface that the client registered in a previous call to the IMMDeviceEnumerator::RegisterEndpointNotificationCallback method.
helpviewer_keywords: ["IMMDeviceEnumerator interface [Core Audio]","UnregisterEndpointNotificationCallback method","IMMDeviceEnumerator.UnregisterEndpointNotificationCallback","IMMDeviceEnumerator::UnregisterEndpointNotificationCallback","IMMDeviceEnumeratorUnregisterEndpointNotificationC","UnregisterEndpointNotificationCallback","UnregisterEndpointNotificationCallback method [Core Audio]","UnregisterEndpointNotificationCallback method [Core Audio]","IMMDeviceEnumerator interface","coreaudio.immdeviceenumerator_unregisterendpointnotificationcallback","mmdeviceapi/IMMDeviceEnumerator::UnregisterEndpointNotificationCallback"]
old-location: coreaudio\immdeviceenumerator_unregisterendpointnotificationcallback.htm
tech.root: CoreAudio
ms.assetid: dc1e85af-f399-469d-806a-a2d80b700b75
ms.date: 12/05/2018
ms.keywords: IMMDeviceEnumerator interface [Core Audio],UnregisterEndpointNotificationCallback method, IMMDeviceEnumerator.UnregisterEndpointNotificationCallback, IMMDeviceEnumerator::UnregisterEndpointNotificationCallback, IMMDeviceEnumeratorUnregisterEndpointNotificationC, UnregisterEndpointNotificationCallback, UnregisterEndpointNotificationCallback method [Core Audio], UnregisterEndpointNotificationCallback method [Core Audio],IMMDeviceEnumerator interface, coreaudio.immdeviceenumerator_unregisterendpointnotificationcallback, mmdeviceapi/IMMDeviceEnumerator::UnregisterEndpointNotificationCallback
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
 - IMMDeviceEnumerator::UnregisterEndpointNotificationCallback
 - mmdeviceapi/IMMDeviceEnumerator::UnregisterEndpointNotificationCallback
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
 - IMMDeviceEnumerator.UnregisterEndpointNotificationCallback
---

# IMMDeviceEnumerator::UnregisterEndpointNotificationCallback


## -description

The <b>UnregisterEndpointNotificationCallback</b> method deletes the registration of a notification interface that the client registered in a previous call to the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.

## -parameters

### -param pClient [in]

Pointer to the client's <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient</a> interface. The client passed this same interface pointer to the device enumerator in a previous call to the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method. For more information, see Remarks.

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
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified notification interface was not found.

</td>
</tr>
</table>

## -remarks

The client must ensure that the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient</a> object is not released after the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">RegisterEndpointNotificationCallback</a> call and before calling <b>UnregisterEndpointNotificationCallback</b>. These methods do not call the client's <b>IMMNotificationClient::AddRef</b> and <b>IMMNotificationClient::Release</b> implementations. The client is responsible for maintaining the reference count of the <b>IMMNotificationClient</b> object. The client must increment the count if the <b>RegisterEndpointNotificationCallback</b> call succeeds and release the final reference only after calling <b>UnregisterEndpointNotificationCallback</b> or implement some other mechanism to ensure that the object is not deleted before <b>UnregisterEndpointNotificationCallback</b> is called. Otherwise, the application leaks the resources held by the <b>IMMNotificationClient</b> and any other object that is implemented in the same container. 



For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>