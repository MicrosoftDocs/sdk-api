---
UID: NF:setupapi.SetupDiSetDevicePropertyW
title: SetupDiSetDevicePropertyW function
author: windows-sdk-content
description: The SetupDiSetDeviceProperty function sets a device instance property.
old-location: devinst\setupdisetdeviceproperty.htm
old-project: devinst
ms.assetid: c03c51ba-3027-4be9-8869-6d7dbeac2428
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: SetupDiSetDeviceProperty, SetupDiSetDeviceProperty function [Device and Driver Installation], SetupDiSetDevicePropertyW, devinst.setupdisetdeviceproperty, di-rtns_ee591571-7fc2-4a2b-a893-ba8d43cc0ed4.xml, setupapi/SetupDiSetDeviceProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Set_DevNode_Property
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceProperty
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiSetDevicePropertyW function


## -description


The <b>SetupDiSetDeviceProperty</b> function sets a device instance property.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a>. This device information set contains a device information element that represents the device instance for which to set a device instance property. 


### -param DeviceInfoData [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that identifies the device instance for which to set a device instance property. 


### -param PropertyKey [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a> structure that represents the device property key of the device instance property to set. 


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff543546">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device instance property. For more information, see the <b>Remarks</b> section later in this topic.


### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the device instance property value. If the property is being deleted or set to a <b>NULL</b> value, this pointer must be <b>NULL</b>, and <i>PropertyBufferSize</i> must be set to zero.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer </i>is <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.


### -param Flags [in]

This parameter must be set to zero.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.

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
<dt><b>ERROR_INVALID_REG_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property key that is supplied by <i>PropertyKey</i> is not valid or the property is not writable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The property-data-type identifier that is supplied by <i>PropertyType</i>, or the property value that is supplied by <i>PropertyBuffer,</i> is not valid. 

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
An unspecified internal element was not found. One possibility is that the property to be deleted does not exist. 

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



<b>SetupDiSetDeviceProperty</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">unified device property model</a>. 

SetupAPI supports only a Unicode version of <b>SetupDiSetDeviceProperty</b>. 

A caller of <b>SetupDiSetDeviceProperty</b> must be a member of the Administrators group to set a device instance property. 

<b>SetupDiSetDeviceProperty</b> enforces requirements on the property-data-type identifier and the property value. 

To obtain the device property keys for the instance device properties that are set for a device, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff551965">SetupDiGetDevicePropertyKeys</a>.

To retrieve a device instance property, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff551963">SetupDiGetDeviceProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551963">SetupDiGetDeviceProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551965">SetupDiGetDevicePropertyKeys</a>
 

 

