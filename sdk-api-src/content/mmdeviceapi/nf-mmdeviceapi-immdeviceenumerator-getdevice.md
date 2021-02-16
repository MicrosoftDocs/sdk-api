---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.GetDevice
title: IMMDeviceEnumerator::GetDevice (mmdeviceapi.h)
description: The GetDevice method retrieves an audio endpoint device that is identified by an endpoint ID string.
helpviewer_keywords: ["GetDevice","GetDevice method [Core Audio]","GetDevice method [Core Audio]","IMMDeviceEnumerator interface","IMMDeviceEnumerator interface [Core Audio]","GetDevice method","IMMDeviceEnumerator.GetDevice","IMMDeviceEnumerator::GetDevice","IMMDeviceEnumeratorGetDevice","coreaudio.immdeviceenumerator_getdevice","mmdeviceapi/IMMDeviceEnumerator::GetDevice"]
old-location: coreaudio\immdeviceenumerator_getdevice.htm
tech.root: CoreAudio
ms.assetid: 88cd7acc-a5d7-406d-ac73-bae357ad2ee2
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Core Audio], GetDevice method [Core Audio],IMMDeviceEnumerator interface, IMMDeviceEnumerator interface [Core Audio],GetDevice method, IMMDeviceEnumerator.GetDevice, IMMDeviceEnumerator::GetDevice, IMMDeviceEnumeratorGetDevice, coreaudio.immdeviceenumerator_getdevice, mmdeviceapi/IMMDeviceEnumerator::GetDevice
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
 - IMMDeviceEnumerator::GetDevice
 - mmdeviceapi/IMMDeviceEnumerator::GetDevice
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
 - IMMDeviceEnumerator.GetDevice
---

# IMMDeviceEnumerator::GetDevice


## -description

The <b>GetDevice</b> method retrieves an audio endpoint device that is identified by an <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a>.

## -parameters

### -param pwstrId [in]

Pointer to a string containing the endpoint ID. The caller typically obtains this string from the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid">IMMDevice::GetId</a> method or from one of the methods in the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient</a> interface.

### -param ppDevice [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface for the specified device. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetDevice</b> call fails,  <i>*ppDevice</i> is <b>NULL</b>.

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
Parameter <i>pwstrId</i> or <i>ppDevice</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The device ID does not identify an audio device that is in this system.

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

If two programs are running in two different processes and both need to access the same audio endpoint device, one program cannot simply pass the device's <b>IMMDevice</b> interface to the other program. However, the programs can access the same device by following these steps:

<ol>
<li>The first program calls the <b>IMMDevice::GetId</b> method in the first process to obtain the endpoint ID string that identifies the device.</li>
<li>The first program passes the endpoint ID string across the process boundary to the second program.</li>
<li>To obtain a reference to the device's <b>IMMDevice</b> interface in the second process, the second program calls <b>GetDevice</b> with the endpoint ID string.</li>
</ol>
For more information about the <b>GetDevice</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/endpoint-id-strings">Endpoint ID Strings</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>
</li>
</ul>
For code examples that use the <b>GetDevice</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/device-events">Device Events</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/using-the-ikscontrol-interface-to-access-audio-properties">Using the IKsControl Interface to Access Audio Properties</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid">IMMDevice::GetId</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>