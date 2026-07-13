---
UID: NF:setupapi.SetupDiGetDevicePropertyKeys
title: SetupDiGetDevicePropertyKeys function (setupapi.h)
description: The SetupDiGetDevicePropertyKeys function retrieves an array of the device property keys that represent the device properties that are set for a device instance.
helpviewer_keywords: ["SetupDiGetDevicePropertyKeys","SetupDiGetDevicePropertyKeys function [Device and Driver Installation]","devinst.setupdigetdevicepropertykeys","di-rtns_49d5f09f-3d86-4292-a389-e6a0ee0946b6.xml","setupapi/SetupDiGetDevicePropertyKeys"]
old-location: devinst\setupdigetdevicepropertykeys.htm
tech.root: devinst
ms.assetid: d4decdab-e412-4719-ad65-74f34cf8df27
ms.date: 12/05/2018
ms.keywords: SetupDiGetDevicePropertyKeys, SetupDiGetDevicePropertyKeys function [Device and Driver Installation], devinst.setupdigetdevicepropertykeys, di-rtns_49d5f09f-3d86-4292-a389-e6a0ee0946b6.xml, setupapi/SetupDiGetDevicePropertyKeys
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_DevNode_Property_Keys
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetDevicePropertyKeys
 - setupapi/SetupDiGetDevicePropertyKeys
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.dll
api_name:
 - SetupDiGetDevicePropertyKeys
---

# SetupDiGetDevicePropertyKeys function


## -description

The <b>SetupDiGetDevicePropertyKeys</b> function retrieves an array of the device property keys that represent the device properties that are set for a device instance.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>. This device information set contains the device instance for which this function retrieves an array of device property keys. The property keys represent the device properties that are set for the device instance.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the device instance for which to retrieve the requested array of device property keys.

### -param PropertyKeyArray [out, optional]

A pointer to a buffer that receives an array of <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device instance. The pointer is optional and can be <b>NULL</b>. For more information, see the <b>Remarks</b> section later in this topic.

### -param PropertyKeyCount [in]

The size, in DEVPROPKEY-typed values, of the <i>PropertyKeyArray </i> buffer<i>. </i>If <i>PropertyKeyArray</i> is set to <b>NULL</b>, <i>PropertyKeyCount</i> must be set to zero.

### -param RequiredPropertyKeyCount [out, optional]

A pointer to a DWORD-typed variable that receives the number of requested device property keys. The pointer is optional and can be set to <b>NULL</b>.

### -param Flags [in]

This parameter must be set to zero.

## -returns

<b>SetupDiGetDevicePropertyKeys</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table includes some of the more common error codes that this function might log. 


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value of<i> Flags</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The device information set that is specified by <i>DevInfoSet</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A supplied parameter is not valid. One possibility is that the device information element is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An internal data value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyKeyArray</i> is <b>NULL</b> and <i>PropertKeyCount</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DEVINST</b></dt>
</dl>
</td>
<td width="60%">
The device instance that is specified by <i>DevInfoData</i> does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>PropertyKeyArray</i> buffer is too small to hold all the requested property keys.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough system memory available to complete the operation.

</td>
</tr>
</table>

## -remarks

<b>SetupDiGetDevicePropertyKeys</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">unified device property model</a>. 

If the <i>ProperKeyArray</i> buffer is not large enough to hold all the requested property keys, <b>SetupDiGetDevicePropertyKeys</b> does not retrieve any property keys and returns ERROR_INSUFFICIENT_BUFFER. If the caller supplied a <i>RequiredPropertyKeyCount</i> pointer, <b>SetupDiGetDevicePropertyKeys</b> sets the value of *<i>RequiredPropertyKeyCount</i> to the required size, in DEVPROPKEY-typed values, of the <i>PropertyKeyArray </i> buffer<i>.</i>

To retrieve a device instance property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a>, and to set a device instance property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdevicepropertyw">SetupDiSetDeviceProperty</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdevicepropertyw">SetupDiSetDeviceProperty</a>