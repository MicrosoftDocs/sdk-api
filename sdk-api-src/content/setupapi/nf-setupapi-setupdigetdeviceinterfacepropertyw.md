---
UID: NF:setupapi.SetupDiGetDeviceInterfacePropertyW
title: SetupDiGetDeviceInterfacePropertyW function (setupapi.h)
description: The SetupDiGetDeviceInterfaceProperty function retrieves a device property that is set for a device interface.
helpviewer_keywords: ["SetupDiGetDeviceInterfaceProperty","SetupDiGetDeviceInterfaceProperty function [Device and Driver Installation]","SetupDiGetDeviceInterfacePropertyW","devinst.setupdigetdeviceinterfaceproperty","di-rtns_7a7e0730-650f-4deb-a724-8f90385c762a.xml","setupapi/SetupDiGetDeviceInterfaceProperty"]
old-location: devinst\setupdigetdeviceinterfaceproperty.htm
tech.root: devinst
ms.assetid: 72a44060-cebc-4690-8776-68db76810732
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInterfaceProperty, SetupDiGetDeviceInterfaceProperty function [Device and Driver Installation], SetupDiGetDeviceInterfacePropertyW, devinst.setupdigetdeviceinterfaceproperty, di-rtns_7a7e0730-650f-4deb-a724-8f90385c762a.xml, setupapi/SetupDiGetDeviceInterfaceProperty
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_Device_Interface_Property
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetDeviceInterfacePropertyW
 - setupapi/SetupDiGetDeviceInterfacePropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-2.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDeviceInterfaceProperty
---

# SetupDiGetDeviceInterfacePropertyW function


## -description

The <b>SetupDiGetDeviceInterfaceProperty</b> function retrieves a device property that is set for a device interface.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device interface for which to retrieve a device interface property.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that represents the device interface for which to retrieve a device interface property.

### -param PropertyKey [in]

A pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the device interface property key of the device interface property to retrieve.

### -param PropertyType [out]

A pointer to a <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed variable that receives the property-data-type identifier of the requested device interface property. The property-data-type identifier is a bitwise OR between a base-data-type identifier and, if the base-data type is modified, a property-data-type modifier.

### -param PropertyBuffer [out]

A pointer to a buffer that receives the requested device interface property. <b>SetupDiGetDeviceInterfaceProperty</b> retrieves the requested property only if the buffer is large enough to hold all the property value data. The pointer can be <b>NULL</b>. If the pointer is set to <b>NULL</b> and <i>RequiredSize</i> is supplied, <b>SetupDiGetDeviceInterfaceProperty</b> returns the size of the property, in bytes, in *<i>RequiredSize</i>.

### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.

### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in bytes, of either the device interface property if the property is retrieved or the required buffer size, if the buffer is not large enough. This pointer can be set to <b>NULL</b>.

### -param Flags [in]

This parameter must be set to zero.

## -returns

<b>SetupDiGetDeviceInterfaceProperty</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table includes some of the more common error codes that this function might log. Other error codes can be set by the device installer functions that are called by this API.


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
A supplied parameter is not valid. One possibility is that the device interface that is specified by <i>DeviceInterfaceData</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_REG_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property key that is supplied by <i>PropertyKey</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An unspecified internal data value was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyBuffer</i> is <b>NULL</b>, and <i>PropertyBufferSize</i> is not zero.

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
The <i>PropertyBuffer</i> buffer is not large enough to hold the property value, or an internal data buffer that was passed to a system call was too small.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested device property does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have Administrator privileges. 

</td>
</tr>
</table>

## -remarks

<b>SetupDiGetDeviceInterfaceProperty</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">unified device property model</a>. 

SetupAPI supports only a Unicode version of <b>SetupDiGetDeviceInterfaceProperty</b>. 

A caller of <b>SetupDiGetDeviceInterfaceProperty</b> must be a member of the Administrators group to set a device interface property. 

To obtain the device property keys that represent the device properties that are set for a device interface, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacepropertykeys">SetupDiGetDeviceInterfacePropertyKeys</a>.

To set a device interface property, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacepropertyw">SetupDiSetDeviceInterfaceProperty</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacepropertykeys">SetupDiGetDeviceInterfacePropertyKeys</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacepropertyw">SetupDiSetDeviceInterfaceProperty</a>