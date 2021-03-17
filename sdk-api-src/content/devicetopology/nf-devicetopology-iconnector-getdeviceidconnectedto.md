---
UID: NF:devicetopology.IConnector.GetDeviceIdConnectedTo
title: IConnector::GetDeviceIdConnectedTo (devicetopology.h)
description: The GetDeviceIdConnectedTo method gets the device identifier of the audio device, if any, that this connector is connected to.
helpviewer_keywords: ["GetDeviceIdConnectedTo","GetDeviceIdConnectedTo method [Core Audio]","GetDeviceIdConnectedTo method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","GetDeviceIdConnectedTo method","IConnector.GetDeviceIdConnectedTo","IConnector::GetDeviceIdConnectedTo","IConnectorGetDeviceIdConnectedTo","coreaudio.iconnector_getdeviceidconnectedto","devicetopology/IConnector::GetDeviceIdConnectedTo"]
old-location: coreaudio\iconnector_getdeviceidconnectedto.htm
tech.root: CoreAudio
ms.assetid: 8f62bdeb-4765-467f-b68d-d94fc9a51dfb
ms.date: 12/05/2018
ms.keywords: GetDeviceIdConnectedTo, GetDeviceIdConnectedTo method [Core Audio], GetDeviceIdConnectedTo method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetDeviceIdConnectedTo method, IConnector.GetDeviceIdConnectedTo, IConnector::GetDeviceIdConnectedTo, IConnectorGetDeviceIdConnectedTo, coreaudio.iconnector_getdeviceidconnectedto, devicetopology/IConnector::GetDeviceIdConnectedTo
req.header: devicetopology.h
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
 - IConnector::GetDeviceIdConnectedTo
 - devicetopology/IConnector::GetDeviceIdConnectedTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IConnector.GetDeviceIdConnectedTo
---

# IConnector::GetDeviceIdConnectedTo


## -description

The <b>GetDeviceIdConnectedTo</b> method gets the device identifier of the audio device, if any, that this connector is connected to.

## -parameters

### -param ppwstrDeviceId [out]

Pointer to a string pointer into which the method writes the address of a null-terminated, wide-character string that contains the device identifier of the connected device. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetDeviceIdConnectedTo</b> call fails,  <i>*ppwstrDeviceId</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
Pointer <i>ppwstrDeviceId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This connector is not connected, or the other side of the connection is not another device topology (for example, a Software_IO connection).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

The device identifier obtained from this method can be used as an input parameter to the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a> method.

This method is functionally equivalent to, but more efficient than, the following series of method calls:

<ul>
<li>Call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a> method to obtain the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface of the "to" connector.</li>
<li>Call the <b>IConnector::QueryInterface</b> method (with parameter <i>iid</i> set to <b>REFIID</b> IID_IPart) to obtain the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of the "to" connector.</li>
<li>Call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-gettopologyobject">IPart::GetTopologyObject</a> method to obtain the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology</a> interface of the "to" device (the device that contains the "to" connector).</li>
<li>Call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getdeviceid">IDeviceTopology::GetDeviceId</a> method to obtain the device ID of the "to" device.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>