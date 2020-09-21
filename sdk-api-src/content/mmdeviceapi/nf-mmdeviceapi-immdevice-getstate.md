---
UID: NF:mmdeviceapi.IMMDevice.GetState
title: IMMDevice::GetState (mmdeviceapi.h)
description: The GetState method retrieves the current device state.
helpviewer_keywords: ["GetState","GetState method [Core Audio]","GetState method [Core Audio]","IMMDevice interface","IMMDevice interface [Core Audio]","GetState method","IMMDevice.GetState","IMMDevice::GetState","IMMDeviceGetState","coreaudio.immdevice_getstate","mmdeviceapi/IMMDevice::GetState"]
old-location: coreaudio\immdevice_getstate.htm
tech.root: CoreAudio
ms.assetid: 9b50773b-241c-4a32-8ab6-85adb3f885e1
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Core Audio], GetState method [Core Audio],IMMDevice interface, IMMDevice interface [Core Audio],GetState method, IMMDevice.GetState, IMMDevice::GetState, IMMDeviceGetState, coreaudio.immdevice_getstate, mmdeviceapi/IMMDevice::GetState
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
 - IMMDevice::GetState
 - mmdeviceapi/IMMDevice::GetState
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
 - IMMDevice.GetState
---

# IMMDevice::GetState


## -description

The <b>GetState</b> method retrieves the current device state.

## -parameters

### -param pdwState [out]

Pointer to a <b>DWORD</b> variable into which the method writes the current state of the device. The device-state value is one of the following <a href="/windows/desktop/CoreAudio/device-state-xxx-constants">DEVICE_STATE_XXX</a> constants:

DEVICE_STATE_ACTIVE

DEVICE_STATE_DISABLED

DEVICE_STATE_NOTPRESENT

DEVICE_STATE_UNPLUGGED

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
Parameter <i>pdwState</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>