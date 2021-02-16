---
UID: NF:devicetopology.IDeviceSpecificProperty.SetValue
title: IDeviceSpecificProperty::SetValue (devicetopology.h)
description: The SetValue method sets the value of the device-specific property.
helpviewer_keywords: ["IDeviceSpecificProperty interface [Core Audio]","SetValue method","IDeviceSpecificProperty.SetValue","IDeviceSpecificProperty::SetValue","IDeviceSpecificPropertySetValue","SetValue","SetValue method [Core Audio]","SetValue method [Core Audio]","IDeviceSpecificProperty interface","coreaudio.idevicespecificproperty_setvalue","devicetopology/IDeviceSpecificProperty::SetValue"]
old-location: coreaudio\idevicespecificproperty_setvalue.htm
tech.root: CoreAudio
ms.assetid: 48e7a638-f602-455f-96d1-9d1eb049a6c0
ms.date: 12/05/2018
ms.keywords: IDeviceSpecificProperty interface [Core Audio],SetValue method, IDeviceSpecificProperty.SetValue, IDeviceSpecificProperty::SetValue, IDeviceSpecificPropertySetValue, SetValue, SetValue method [Core Audio], SetValue method [Core Audio],IDeviceSpecificProperty interface, coreaudio.idevicespecificproperty_setvalue, devicetopology/IDeviceSpecificProperty::SetValue
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
 - IDeviceSpecificProperty::SetValue
 - devicetopology/IDeviceSpecificProperty::SetValue
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
 - IDeviceSpecificProperty.SetValue
---

# IDeviceSpecificProperty::SetValue


## -description

The <b>SetValue</b> method sets the value of the device-specific property.

## -parameters

### -param pvValue [in]

Pointer to the new value for the device-specific property.

### -param cbValue [in]

The size in bytes of the device-specific property value.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetValue</b> call changes the state of the control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
Pointer <i>pvValue</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>cbValue</i> does not match the required size of the property value.

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

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty Interface</a>