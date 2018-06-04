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

# SetupDiGetCustomDevicePropertyA function


## -description


The <b>SetupDiGetCustomDeviceProperty</b> function retrieves a specified custom device property from the registry.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to retrieve a custom device property. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. 


### -param CustomPropertyName [in]

A registry value name representing a custom property.


### -param Flags [in]

A flag value that indicates how the requested information should be returned. The flag can be zero or one of the following:





#### DICUSTOMDEVPROP_MERGE_MULTISZ

If set, the function retrieves both device instance-specific property values and hardware ID-specific property values, concatenated as a REG_MULTI_SZ-typed string. (For more information, see the <b>Remarks</b> section on this reference page.)


### -param PropertyRegDataType [out, optional]

A pointer to a variable of type DWORD that receives the data type of the retrieved property. The data type is specified as one of the REG_-prefixed constants that represents registry data types. This parameter is optional and can be <b>NULL</b>.


### -param PropertyBuffer [out]

A pointer to a buffer that receives requested property information.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer </i>buffer.


### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the buffer size, in bytes, that is required to receive the requested information. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetCustomDeviceProperty</b> returns the required size, regardless of whether the <i>PropertyBuffer</i> buffer is large enough to receive the requested information.


## -returns



If the operation succeeds, <b>SetupDiGetCustomDeviceProperty</b> returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>. If the <i>PropertyBuffer </i>buffer is not large enough to receive the requested information, <b>SetupDiGetCustomDeviceProperty</b> returns <b>FALSE</b> and a subsequent call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER.




## -remarks



<b>SetupDiGetCustomDeviceProperty</b> retrieves device properties that are associated with a single device instance or with all devices matching a certain hardware ID. (For information about hardware IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>).

Vendors can set properties for a device instance by using <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/inf-addreg-directive">INF AddReg directives</a> in <a href="devinst.inf_ddinstall_hw_section">INF DDInstall.HW sections</a> and specifying the <b>HKR</b> registry root.

Only the system can set properties for hardware IDs. The system supplies an "Icon" property for some hardware IDs.

The function first checks to see if the specified property exists for the specified device instance. If so, the property's value is returned. If not, the function checks to see if the property exists for all devices matching the hardware ID of the specified device instance. If so, the property's value is returned. If DICUSTOMDEVPROP_MERGE_MULTISZ is set in <i>Flags</i>, the function returns the property values associated with both the device instance and the hardware ID, if they both exist.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551097">SetupDiGetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552079">SetupDiOpenDevRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552135">SetupDiSetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552169">SetupDiSetDeviceRegistryProperty</a>
 

 

