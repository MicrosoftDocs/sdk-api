---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# MFCreateSensorGroup function


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> interface based on the provided symbolic link name.


## -parameters




### -param SensorGroupSymbolicLink

The symbolic link for the new <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>. This name can be obtained through device enumeration APIs such as This is the symbolic link name obtained through either the standard Win32 device enumeration, such as <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a> or <a href="https://msdn.microsoft.com/da4d96ce-e22b-4e1c-aa2e-df46416a5f0b">MFEnumDeviceSources</a> or by getting the  <a href="https://docs.microsoft.com/en-us/uwp/api/Windows.Devices.Enumeration.DeviceInformation">Id</a> property of the <a href="https://docs.microsoft.com/en-us/uwp/api/Windows.Devices.Enumeration.DeviceInformation">DeviceInformation</a> class.


### -param ppSensorGroup [out]

The symbolic link for the new <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <b>LPCWSTR</b> is null.

</td>
</tr>
</table>
 




## -remarks



If the function succeeds, <i>ppSesnorGroup</i> will point to a valid <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> object.  The caller must release this interface.

<div class="alert"><b>Note</b>  When this API is used with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff548567(v=vs.85).aspx">KSCATEGORY_SENSOR_CAMERA</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff548567(v=vs.85).aspx">KSCATEGORY_VIDEO_CAMERA</a> symbolic name, the resulting <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> object will only contain one sensor device but behaves as a virtualized sensor group.  The caller  may use the resulting object in the same manner as a sensor group obtained from a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff548567(v=vs.85).aspx">KSCATEGORY_SENSOR_GROUP</a>.</div>
<div> </div>


