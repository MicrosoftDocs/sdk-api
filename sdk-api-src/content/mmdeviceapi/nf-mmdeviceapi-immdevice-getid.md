---
UID: NF:mmdeviceapi.IMMDevice.GetId
title: IMMDevice::GetId (mmdeviceapi.h)
description: The GetId method retrieves an endpoint ID string that identifies the audio endpoint device.
helpviewer_keywords: ["GetId","GetId method [Core Audio]","GetId method [Core Audio]","IMMDevice interface","IMMDevice interface [Core Audio]","GetId method","IMMDevice.GetId","IMMDevice::GetId","IMMDeviceGetId","coreaudio.immdevice_getid","mmdeviceapi/IMMDevice::GetId"]
old-location: coreaudio\immdevice_getid.htm
tech.root: CoreAudio
ms.assetid: b2f56713-856c-408e-8993-1d13e234dc89
ms.date: 12/05/2018
ms.keywords: GetId, GetId method [Core Audio], GetId method [Core Audio],IMMDevice interface, IMMDevice interface [Core Audio],GetId method, IMMDevice.GetId, IMMDevice::GetId, IMMDeviceGetId, coreaudio.immdevice_getid, mmdeviceapi/IMMDevice::GetId
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
 - IMMDevice::GetId
 - mmdeviceapi/IMMDevice::GetId
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
 - IMMDevice.GetId
---

# IMMDevice::GetId


## -description

The <b>GetId</b> method retrieves an <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device.

## -parameters

### -param ppstrId [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string containing the endpoint device ID. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetId</b> call fails,  <i>*ppstrId is NULL.</i> For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pwstrId</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The endpoint ID string obtained from this method identifies the audio endpoint device that is represented by the <b>IMMDevice</b> interface instance. A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a> method. Clients should treat the contents of the endpoint ID string as opaque. That is, clients should <i>not</i> attempt to parse the contents of the string to obtain information about the device. The reason is that the string format is undefined and might change from one implementation of the MMDevice API system module to the next.

For code examples that call the <b>GetId</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/device-roles-for-legacy-windows-multimedia-applications">Device Roles for Legacy Windows Multimedia Applications</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>