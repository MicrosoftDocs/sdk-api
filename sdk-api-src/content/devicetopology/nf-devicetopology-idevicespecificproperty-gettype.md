---
UID: NF:devicetopology.IDeviceSpecificProperty.GetType
title: IDeviceSpecificProperty::GetType (devicetopology.h)
description: The GetType method gets the data type of the device-specific property value.
helpviewer_keywords: ["GetType","GetType method [Core Audio]","GetType method [Core Audio]","IDeviceSpecificProperty interface","IDeviceSpecificProperty interface [Core Audio]","GetType method","IDeviceSpecificProperty.GetType","IDeviceSpecificProperty::GetType","IDeviceSpecificPropertyGetType","coreaudio.idevicespecificproperty_gettype","devicetopology/IDeviceSpecificProperty::GetType"]
old-location: coreaudio\idevicespecificproperty_gettype.htm
tech.root: CoreAudio
ms.assetid: 07d32eea-e80a-4f25-b963-3f667e56a811
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Core Audio], GetType method [Core Audio],IDeviceSpecificProperty interface, IDeviceSpecificProperty interface [Core Audio],GetType method, IDeviceSpecificProperty.GetType, IDeviceSpecificProperty::GetType, IDeviceSpecificPropertyGetType, coreaudio.idevicespecificproperty_gettype, devicetopology/IDeviceSpecificProperty::GetType
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
 - IDeviceSpecificProperty::GetType
 - devicetopology/IDeviceSpecificProperty::GetType
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
 - IDeviceSpecificProperty.GetType
---

# IDeviceSpecificProperty::GetType


## -description

The <b>GetType</b> method gets the data type of the device-specific property value.

## -parameters

### -param pVType [out]

Pointer to a <b>VARTYPE</b> variable into which the method writes a <b>VARTYPE</b> enumeration value that indicates the data type of the device-specific property value. For more information about <b>VARTYPE</b> and <b>VARTYPE</b>, see the Windows SDK documentation.

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
Pointer <i>pVType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty Interface</a>