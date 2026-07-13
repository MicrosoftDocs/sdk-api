---
UID: NF:setupapi.SetupDiGetDeviceInterfacePropertyKeys
title: SetupDiGetDeviceInterfacePropertyKeys function (setupapi.h)
description: The SetupDiGetDeviceInterfacePropertyKeys function retrieves an array of device property keys that represent the device properties that are set for a device interface.
helpviewer_keywords: ["SetupDiGetDeviceInterfacePropertyKeys","SetupDiGetDeviceInterfacePropertyKeys function [Device and Driver Installation]","devinst.setupdigetdeviceinterfacepropertykeys","di-rtns_0f8848a9-4efc-408e-828a-6279294e6cf5.xml","setupapi/SetupDiGetDeviceInterfacePropertyKeys"]
old-location: devinst\setupdigetdeviceinterfacepropertykeys.htm
tech.root: devinst
ms.assetid: 46eedc41-17ee-4306-ad34-22bfd98cb96b
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInterfacePropertyKeys, SetupDiGetDeviceInterfacePropertyKeys function [Device and Driver Installation], devinst.setupdigetdeviceinterfacepropertykeys, di-rtns_0f8848a9-4efc-408e-828a-6279294e6cf5.xml, setupapi/SetupDiGetDeviceInterfacePropertyKeys
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_Device_Interface_Property_Keys
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
 - SetupDiGetDeviceInterfacePropertyKeys
 - setupapi/SetupDiGetDeviceInterfacePropertyKeys
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
 - SetupDiGetDeviceInterfacePropertyKeys
---

# SetupDiGetDeviceInterfacePropertyKeys function


## -description

The <b>SetupDiGetDeviceInterfacePropertyKeys</b> function retrieves an array of device property keys that represent the device properties that are set for a device interface.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>. This device information set contains a device interface for which to retrieve an array of the device property keys that represent the device properties that are set for a device interface.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that represents the device interface for which to retrieve the requested array of device property keys.

### -param PropertyKeyArray [out, optional]

A pointer to a buffer that receives an array of <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed values, where each value is a device property key for a device property that is set for the device interface. The pointer is optional and can be <b>NULL</b>. For more information, see the <b>Remarks</b> section later in this topic.

### -param PropertyKeyCount [in]

The size, in DEVPROPKEY-typed elements, of the <i>PropertyKeyArray </i> buffer<i>. </i>If <i>PropertyKeyArray</i> is <b>NULL</b>, <i>PropertyKeyCount</i> must be set to zero.

### -param RequiredPropertyKeyCount [out, optional]

A pointer to a DWORD-typed variable that receives the number of requested device property keys. The pointer is optional and can be set to <b>NULL</b>.

### -param Flags [in]

This parameter must be set to zero.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid. One possibility is that the device interface that is specified by <i>DevInterfaceData</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyKeyArray</i> is <b>NULL</b>, and <i>PropertKeyCount</i> is not zero. .

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DEVICE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The device interface that is specified by <i>DeviceInterfaceData</i> does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>PropertyKeyArray</i> buffer is not large enough to hold all the requested property keys.

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

<b>SetupDiGetDeviceInterfacePropertyKeys</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">unified device property model</a>. 

If the <i>PropertyKeyArray</i> buffer is not large enough to hold all the requested property keys, <b>SetupDiGetDeviceInterfacePropertyKeys</b> does not retrieve any property keys and returns ERROR_INSUFFICIENT_BUFFER. If the caller supplied a <i>RequiredPropertyKeyCount</i> pointer, <b>SetupDiGetDeviceInterfacePropertyKeys</b> sets the value of *<i>RequiredPropertyKeyCount</i> to the required size, in DEVPROPKEY-typed values, of the <i>PropertyKeyArray </i> buffer<i>.</i>

To retrieve a device interface property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacepropertyw">SetupDiGetDeviceInterfaceProperty</a><b>,</b> and to set a device interface property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacepropertyw">SetupDiSetDeviceInterfaceProperty</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacepropertyw">SetupDiGetDeviceInterfaceProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacepropertyw">SetupDiSetDeviceInterfaceProperty</a>