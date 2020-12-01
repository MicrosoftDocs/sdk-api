---
UID: NF:devicetopology.IDeviceTopology.GetDeviceId
title: IDeviceTopology::GetDeviceId (devicetopology.h)
description: The GetDeviceId method gets the device identifier of the device that is represented by the device-topology object.
helpviewer_keywords: ["GetDeviceId","GetDeviceId method [Core Audio]","GetDeviceId method [Core Audio]","IDeviceTopology interface","IDeviceTopology interface [Core Audio]","GetDeviceId method","IDeviceTopology.GetDeviceId","IDeviceTopology::GetDeviceId","IDeviceTopologyGetDeviceId","coreaudio.idevicetopology_getdeviceid","devicetopology/IDeviceTopology::GetDeviceId"]
old-location: coreaudio\idevicetopology_getdeviceid.htm
tech.root: CoreAudio
ms.assetid: 2ecf8f23-7cfd-447a-ab76-8a23b79f5d6c
ms.date: 12/05/2018
ms.keywords: GetDeviceId, GetDeviceId method [Core Audio], GetDeviceId method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetDeviceId method, IDeviceTopology.GetDeviceId, IDeviceTopology::GetDeviceId, IDeviceTopologyGetDeviceId, coreaudio.idevicetopology_getdeviceid, devicetopology/IDeviceTopology::GetDeviceId
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
 - IDeviceTopology::GetDeviceId
 - devicetopology/IDeviceTopology::GetDeviceId
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
 - IDeviceTopology.GetDeviceId
---

# IDeviceTopology::GetDeviceId


## -description

The <b>GetDeviceId</b> method gets the device identifier of the device that is represented by the device-topology object.

## -parameters

### -param ppwstrDeviceId [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the device identifier. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetDeviceId</b> call fails,  <i>*ppwstrDeviceId</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
<dt><b>D_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppwstrDeviceId</i> is <b>NULL</b>.

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

The device identifier obtained from this method can be used as an input parameter to the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a> method.

For a code example that uses the <b>GetDeviceId</b> method, see <a href="/windows/desktop/CoreAudio/using-the-ikscontrol-interface-to-access-audio-properties">Using the IKsControl Interface to Access Audio Properties</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>