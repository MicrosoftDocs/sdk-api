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

# SetupDiOpenDeviceInfoA function


## -description


The <b>SetupDiOpenDeviceInfo</b> function adds a device information element for a device instance to a device information set, if one does not already exist in the device information set, and retrieves information that identifies the device information element for the device instance in the device information set.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> to which <b>SetupDiOpenDeviceInfo</b> adds a device information element, if one does not already exist, for the device instance that is specified by <i>DeviceInstanceId</i>. 


### -param DeviceInstanceId [in]

A pointer to a NULL-terminated string that supplies the device instance identifier of a device (for example, "Root\*PNP0500\0000"). If <i>DeviceInstanceId</i> is <b>NULL</b> or references a zero-length string, <b>SetupDiOpenDeviceInfo</b> adds a device information element to the supplied device information set, if one does not already exist, for the root device in the device tree. 


### -param hwndParent [in, optional]

The handle to the top-level window to use for any user interface related to installing the device.


### -param OpenFlags [in]

A variable of DWORD type that controls how the device information element is opened. The value of this parameter can be one or more of the following:





#### DIOD_CANCEL_REMOVE

If this flag is specified and the device had been marked for pending removal, the operating system cancels the pending removal.



#### DIOD_INHERIT_CLASSDRVS

If this flag is specified, the resulting device information element inherits the class driver list, if any, associated with the device information set. In addition, if there is a selected driver for the device information set, that same driver is selected for the new device information element.

If the device information element was already present, its class driver list, if any, is replaced with the inherited list.


### -param DeviceInfoData [out, optional]

A pointer to a caller-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that receives information about the device information element for the device instance that is specified by <i>DeviceInstanceId</i>. The caller must set <b>cbSize</b> to <b>sizeof(</b>SP_DEVINFO_DATA<b>)</b>. This parameter is optional and can be <b>NULL</b>. 


## -returns



<b>SetupDiOpenDeviceInfo</b> returns <b>TRUE</b> if it is successful. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If this device instance is being added to a set that has an associated class, the device class must be the same or the call will fail. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_CLASS_MISMATCH.

If the new device information element is successfully opened but the caller-supplied <i>DeviceInfoData</i> buffer is invalid, this function returns <b>FALSE</b>. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_USER_BUFFER. However, the device information element is added as a new member of the set anyway.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550952">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550978">SetupDiDeleteDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551010">SetupDiEnumDeviceInfo</a>
 

 

