---
UID: NF:devicetopology.IDeviceSpecificProperty.Get4BRange
title: IDeviceSpecificProperty::Get4BRange (devicetopology.h)
description: The Get4BRange method gets the 4-byte range of the device-specific property value.
helpviewer_keywords: ["Get4BRange","Get4BRange method [Core Audio]","Get4BRange method [Core Audio]","IDeviceSpecificProperty interface","IDeviceSpecificProperty interface [Core Audio]","Get4BRange method","IDeviceSpecificProperty.Get4BRange","IDeviceSpecificProperty::Get4BRange","IDeviceSpecificPropertyGet4BRange","coreaudio.idevicespecificproperty_get4brange","devicetopology/IDeviceSpecificProperty::Get4BRange"]
old-location: coreaudio\idevicespecificproperty_get4brange.htm
tech.root: CoreAudio
ms.assetid: 16ca72b5-2de2-4644-9c64-cdc69a9b2c51
ms.date: 12/05/2018
ms.keywords: Get4BRange, Get4BRange method [Core Audio], Get4BRange method [Core Audio],IDeviceSpecificProperty interface, IDeviceSpecificProperty interface [Core Audio],Get4BRange method, IDeviceSpecificProperty.Get4BRange, IDeviceSpecificProperty::Get4BRange, IDeviceSpecificPropertyGet4BRange, coreaudio.idevicespecificproperty_get4brange, devicetopology/IDeviceSpecificProperty::Get4BRange
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
 - IDeviceSpecificProperty::Get4BRange
 - devicetopology/IDeviceSpecificProperty::Get4BRange
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
 - IDeviceSpecificProperty.Get4BRange
---

# IDeviceSpecificProperty::Get4BRange


## -description

The <b>Get4BRange</b> method gets the 4-byte range of the device-specific property value.

## -parameters

### -param plMin [out]

Pointer to a <b>LONG</b> variable into which the method writes the minimum property value.

### -param plMax [out]

Pointer to a <b>LONG</b> variable into which the method writes the maximum property value.

### -param plStepping [out]

Pointer to a <b>LONG</b> variable into which the method writes the stepping value between consecutive property values in the range  <i>*plMin</i> to  <i>*plMax</i>. If the difference between the maximum and minimum property values is <i>d</i>, and the range is divided into <i>n</i> steps (uniformly sized intervals), then the property can take <i>n</i> + 1 discrete values and the size of the step between consecutive values is d / n.

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
Pointer <i>plMin</i>, <i>plMax</i>, or <i>plStepping</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The property value is not a 32-bit signed or unsigned integer. For information about this macro, see the Windows SDK documentation.

</td>
</tr>
</table>

## -remarks

This method reports the range and step size for a property value that is a 32-bit signed or unsigned integer. These two data types are represented by <b>VARENUM</b> enumeration constants VT_I4 and VT_UI4, respectively. If the property value is not a 32-bit integer, then the method returns an error status code. For more information about <b>VARENUM</b>, see the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicespecificproperty">IDeviceSpecificProperty Interface</a>