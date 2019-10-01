---
UID: NF:setupapi.SetupDiGetCustomDevicePropertyA
title: SetupDiGetCustomDevicePropertyA function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetCustomDeviceProperty function retrieves a specified custom device property from the registry.
old-location: devinst\setupdigetcustomdeviceproperty.htm
tech.root: devinst
ms.assetid: 5b8f58ce-0f6f-4de3-82c8-6cfa7c842edc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiGetCustomDeviceProperty, SetupDiGetCustomDeviceProperty function [Device and Driver Installation], SetupDiGetCustomDevicePropertyA, SetupDiGetCustomDevicePropertyW, devinst.setupdigetcustomdeviceproperty, di-rtns_ec69099c-ea3f-47f8-bc14-c10dbd7cba0e.xml, setupapi/SetupDiGetCustomDeviceProperty, setupapi/SetupDiGetCustomDevicePropertyA, setupapi/SetupDiGetCustomDevicePropertyW
ms.topic: function
f1_keywords:
- setupapi/SetupDiGetCustomDeviceProperty
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDiGetCustomDevicePropertyW (Unicode) and SetupDiGetCustomDevicePropertyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- setupapi.dll
api_name:
- SetupDiGetCustomDeviceProperty
- SetupDiGetCustomDevicePropertyA
- SetupDiGetCustomDevicePropertyW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetCustomDevicePropertyA function


## -description


The <b>SetupDiGetCustomDeviceProperty</b> function retrieves a specified custom device property from the registry.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to retrieve a custom device property. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. 


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

Vendors can set properties for a device instance by using <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/inf-addreg-directive">INF AddReg directives</a> in <a href="https://docs.microsoft.com/windows-hardware/drivers/install/inf-ddinstall-hw-section">INF DDInstall.HW sections</a> and specifying the <b>HKR</b> registry root.

Only the system can set properties for hardware IDs. The system supplies an "Icon" property for some hardware IDs.

The function first checks to see if the specified property exists for the specified device instance. If so, the property's value is returned. If not, the function checks to see if the property exists for all devices matching the hardware ID of the specified device instance. If so, the property's value is returned. If DICUSTOMDEVPROP_MERGE_MULTISZ is set in <i>Flags</i>, the function returns the property values associated with both the device instance and the hardware ID, if they both exist.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassregistrypropertya">SetupDiGetClassRegistryProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceregistrypropertya">SetupDiGetDeviceRegistryProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassregistrypropertya">SetupDiSetClassRegistryProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya">SetupDiSetDeviceRegistryProperty</a>
 

 

