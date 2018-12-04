---
UID: NF:setupapi.SetupDiSetDeviceInterfacePropertyW
title: SetupDiSetDeviceInterfacePropertyW function
author: windows-sdk-content
description: The SetupDiSetDeviceInterfaceProperty function sets a device property of a device interface.
old-location: devinst\setupdisetdeviceinterfaceproperty.htm
tech.root: devinst
ms.assetid: 5c8da8a3-1c53-42c1-8adc-46743b63f731
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SetupDiSetDeviceInterfaceProperty, SetupDiSetDeviceInterfaceProperty , SetupDiSetDeviceInterfaceProperty function [Device and Driver Installation], SetupDiSetDeviceInterfacePropertyW, devinst.setupdisetdeviceinterfaceproperty, di-rtns_046f3d0e-43cc-4a62-be1e-4bbad8e59e48.xml, setupapi/SetupDiSetDeviceInterfaceProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Set_Device_Interface_Property
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceInterfaceProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiSetDeviceInterfacePropertyW function


## -description


The <b>SetupDiSetDeviceInterfaceProperty</b> function sets a device property of a device interface.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains the device interface for which to set a device interface property.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure that represents the device interface for which to set a device interface property.


### -param PropertyKey [in]

A pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the device property key of the device interface property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier of the device interface property to set. For more information about the property-data-type identifier, see the <b>Remarks</b> section later in this topic.


### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the device interface property value. If either the property or the interface value is being deleted, this pointer must be set to <b>NULL</b>, and <i>PropertyBufferSize</i> must be set to zero. For more information about property value data, see the <b>Remarks</b> section later in this topic.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. The property buffer size must be consistent with the property-data-type identifier that is supplied by <i>PropertyType</i>. If <i>PropertyBuffer </i>is set to <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.


### -param Flags [in]

Must be set to zero.


## -returns



<b>SetupDiSetDeviceInterfaceProperty</b> returns <b>TRUE</b> if it is successful. Otherwise, this function returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.

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
A supplied parameter is not valid. One possibility is that the device interface specified by <i>DeviceInterfaceData</i> is not valid.

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
An unspecified data value was not valid. This error could be logged if either the symbolic link name of the device interface is not valid or the property-data-type identifier is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyBuffer</i> is <b>NULL</b>, and <i>PropertBufferSize</i> is not zero.

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
An internal data buffer that was passed to a system call was too small.

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
An unspecified internal element was not found. One possibility is that a property to be deleted does not exist. 

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



<b>SetupDiSetDeviceInterfaceProperty</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">unified device property model</a>. 

SetupAPI supports only a Unicode version of <b>SetupDiSetDeviceInterfaceProperty</b>. 

A caller of <b>SetupDiSetDeviceInterfaceProperty</b> must be a member of the Administrators group to set a device interface property. 

<b>SetupDiSetDeviceInterfaceProperty</b> enforces requirements on the property-data-type identifier and the property value. 

To obtain the device property keys that represent the device properties that are set for a device interface, call <a href="https://msdn.microsoft.com/46eedc41-17ee-4306-ad34-22bfd98cb96b">SetupDiGetDeviceInterfacePropertyKeys</a>.

To retrieve a device interface property, call <a href="https://msdn.microsoft.com/72a44060-cebc-4690-8776-68db76810732">SetupDiGetDeviceInterfaceProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/72a44060-cebc-4690-8776-68db76810732">SetupDiGetDeviceInterfaceProperty</a>



<a href="https://msdn.microsoft.com/46eedc41-17ee-4306-ad34-22bfd98cb96b">SetupDiGetDeviceInterfacePropertyKeys</a>
 

 

