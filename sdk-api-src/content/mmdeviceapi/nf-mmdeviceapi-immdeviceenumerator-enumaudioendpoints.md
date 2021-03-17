---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.EnumAudioEndpoints
title: IMMDeviceEnumerator::EnumAudioEndpoints (mmdeviceapi.h)
description: The EnumAudioEndpoints method generates a collection of audio endpoint devices that meet the specified criteria.
helpviewer_keywords: ["EnumAudioEndpoints","EnumAudioEndpoints method [Core Audio]","EnumAudioEndpoints method [Core Audio]","IMMDeviceEnumerator interface","IMMDeviceEnumerator interface [Core Audio]","EnumAudioEndpoints method","IMMDeviceEnumerator.EnumAudioEndpoints","IMMDeviceEnumerator::EnumAudioEndpoints","IMMDeviceEnumeratorEnumAudioEndpoints","coreaudio.immdeviceenumerator_enumaudioendpoints","mmdeviceapi/IMMDeviceEnumerator::EnumAudioEndpoints"]
old-location: coreaudio\immdeviceenumerator_enumaudioendpoints.htm
tech.root: CoreAudio
ms.assetid: ebdd2dcd-82c5-423f-a85d-04388f5078ec
ms.date: 12/05/2018
ms.keywords: EnumAudioEndpoints, EnumAudioEndpoints method [Core Audio], EnumAudioEndpoints method [Core Audio],IMMDeviceEnumerator interface, IMMDeviceEnumerator interface [Core Audio],EnumAudioEndpoints method, IMMDeviceEnumerator.EnumAudioEndpoints, IMMDeviceEnumerator::EnumAudioEndpoints, IMMDeviceEnumeratorEnumAudioEndpoints, coreaudio.immdeviceenumerator_enumaudioendpoints, mmdeviceapi/IMMDeviceEnumerator::EnumAudioEndpoints
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
 - IMMDeviceEnumerator::EnumAudioEndpoints
 - mmdeviceapi/IMMDeviceEnumerator::EnumAudioEndpoints
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
 - IMMDeviceEnumerator.EnumAudioEndpoints
---

# IMMDeviceEnumerator::EnumAudioEndpoints


## -description

The <b>EnumAudioEndpoints</b> method generates a collection of audio endpoint devices that meet the specified criteria.

## -parameters

### -param dataFlow [in]

The data-flow direction for the endpoint devices in the collection. The caller should set this parameter to one of the following <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow">EDataFlow</a> enumeration values:

eRender

eCapture

eAll

If the caller specifies eAll, the method includes both rendering and capture endpoints in the collection.

### -param dwStateMask [in]

The state or states of the endpoints that are to be included in the collection. The caller should set this parameter to the bitwise OR of one or more of the following <a href="/windows/desktop/CoreAudio/device-state-xxx-constants">DEVICE_STATE_XXX</a> constants:

DEVICE_STATE_ACTIVE

DEVICE_STATE_DISABLED

DEVICE_STATE_NOTPRESENT

DEVICE_STATE_UNPLUGGED

For example, if the caller sets the <i>dwStateMask</i> parameter to DEVICE_STATE_ACTIVE | DEVICE_STATE_UNPLUGGED, the method includes endpoints that are either active or unplugged from their jacks, but excludes endpoints that are on audio adapters that have been disabled or are not present. To include all endpoints, regardless of state, set <i>dwStateMask</i> = DEVICE_STATEMASK_ALL.

### -param ppDevices [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection</a> interface of the device-collection object. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>EnumAudioEndpoints</b> call fails,  <i>*ppDevices</i> is <b>NULL</b>.

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
Parameter <i>ppDevices</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>dataFlow</i> or <i>dwStateMask</i> is out of range.

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

For example, the following call enumerates all audio-rendering endpoint devices that are currently active (present and not disabled):


```cpp

  hr = pDevEnum->EnumAudioEndpoints(
                   eRender, DEVICE_STATE_ACTIVE,
                   &pEndpoints);

```


In the preceding code fragment, variable <i>hr</i> is of type <b>HRESULT</b>, <i>pDevEnum</i> is a pointer to an <b>IMMDeviceEnumerator</b> interface, and <i>pEndpoints</i> is a pointer to an <b>IMMDeviceCollection</b> interface.


#### Examples

For a code example that calls the <b>EnumAudioEndpoints</b> method, see <a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>