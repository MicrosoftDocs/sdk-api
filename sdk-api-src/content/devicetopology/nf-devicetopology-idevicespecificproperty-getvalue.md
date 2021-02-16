---
UID: NF:devicetopology.IDeviceSpecificProperty.GetValue
title: IDeviceSpecificProperty::GetValue (devicetopology.h)
description: The GetValue method gets the current value of the device-specific property.
helpviewer_keywords: ["GetValue","GetValue method [Core Audio]","GetValue method [Core Audio]","IDeviceSpecificProperty interface","IDeviceSpecificProperty interface [Core Audio]","GetValue method","IDeviceSpecificProperty.GetValue","IDeviceSpecificProperty::GetValue","IDeviceSpecificPropertyGetValue","coreaudio.idevicespecificproperty_getvalue","devicetopology/IDeviceSpecificProperty::GetValue"]
old-location: coreaudio\idevicespecificproperty_getvalue.htm
tech.root: CoreAudio
ms.assetid: 07608b42-972c-4d5a-9e1c-5d9060f16644
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Core Audio], GetValue method [Core Audio],IDeviceSpecificProperty interface, IDeviceSpecificProperty interface [Core Audio],GetValue method, IDeviceSpecificProperty.GetValue, IDeviceSpecificProperty::GetValue, IDeviceSpecificPropertyGetValue, coreaudio.idevicespecificproperty_getvalue, devicetopology/IDeviceSpecificProperty::GetValue
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
 - IDeviceSpecificProperty::GetValue
 - devicetopology/IDeviceSpecificProperty::GetValue
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
 - IDeviceSpecificProperty.GetValue
---

# IDeviceSpecificProperty::GetValue


## -description

The <b>GetValue</b> method gets the current value of the device-specific property.

## -parameters

### -param pvValue [out]

Pointer to a caller-allocated buffer into which the method writes the property value.

### -param pcbValue

[inout] Pointer to a <b>DWORD</b> variable that specifies the size in bytes of the property value. On entry,  <i>*pcbValue</i> contains the size of the caller-allocated buffer (or 0 if <i>pvValue</i> is <b>NULL</b>). Before returning, the method writes the actual size of the property value written to the buffer (or the required size if the buffer is too small or if <i>pvValue</i> is <b>NULL</b>).

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
Pointer <i>pcbValue</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by parameter <i>pvValue</i> is too small to contain the property value, or <i>pvValue</i> is <b>NULL</b> and the size of the property value is fixed rather than variable. For information about this macro, see the Windows SDK documentation.

</td>
</tr>
</table>

## -remarks

If the size of the property value is variable rather than fixed, the caller can obtain the required buffer size by calling <b>GetValue</b> with parameter <i>pvValue</i> = <b>NULL</b> and  <i>*pcbValue</i> = 0. The method writes the required buffer size to  <i>*pcbValue</i>. With this information, the caller can allocate a buffer of the required size and call <b>GetValue</b> a second time to obtain the property value.

If the caller-allocated buffer is too small to hold the property value, <b>GetValue</b> writes the required buffer size to  <i>*pcbValue</i> and returns an error status code. In this case, it writes nothing to the buffer pointed by <i>pvValue</i>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty Interface</a>