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

# SetupDiGetClassRegistryPropertyW function


## -description


The <b>SetupDiGetClassRegistryProperty</b> function retrieves a property for a specified <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> from the registry.


## -parameters




### -param ClassGuid [in]

A pointer to a GUID representing the device setup class for which a property is to be retrieved.


### -param Property [in]

A value that identifies the property to be retrieved. This must be one of the following values:





#### SPCRP_CHARACTERISTICS

The function returns flags indicating device characteristics for the class. For a list of characteristics flags, see the <i>DeviceCharacteristics</i> parameter to <a href="https://msdn.microsoft.com/library/windows/hardware/ff548397">IoCreateDevice</a>.



#### SPCRP_DEVTYPE

The function returns a DWORD value that represents the device type for the class. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563821">Specifying Device Types</a>.



#### SPCRP_EXCLUSIVE

The function returns a DWORD value indicating whether users can obtain exclusive access to devices for this class. The returned value is one if exclusive access is allowed, or zero otherwise.



#### SPCRP_LOWERFILTERS

(Windows Vista and later) The function returns a REG_MULTI_SZ list of the service names of the lower filter drivers that are installed for the device setup class.



#### SPCRP_SECURITY

The function returns the device's security descriptor as a SECURITY_DESCRIPTOR structure in self-relative format (described in the Microsoft Windows SDK documentation).



#### SPCRP_SECURITY_SDS

The function returns the device's security descriptor as a text string. For information about security descriptor strings, see <a href="https://msdn.microsoft.com/2b15325e-34ed-497b-ae6d-3ec3ac168232">Security Descriptor Definition Language (Windows)</a>. For information about the format of security descriptor strings, see Security Descriptor Definition Language (Windows).



#### SPCRP_UPPERFILTERS

(Windows Vista and later) The function returns a REG_MULTI_SZ list of the service names of the upper filter drivers that are installed for the device setup class.


### -param PropertyRegDataType [out, optional]

A pointer to a variable of type DWORD that receives the property data type as one of the REG_-prefixed registry data types. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, S<b>etupDiGetClassRegistryProperty</b> does not return the data type.


### -param PropertyBuffer [out]

A pointer to a buffer that receives the requested property. 


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer </i>buffer.


### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the required size, in bytes, of the <i>PropertyBuffer </i>buffer. If the <i>PropertyBuffer</i> buffer is too small, and <i>RequiredSize</i> is not <b>NULL</b>, the function sets <i>RequiredSize</i> to the minimum buffer size that is required to receive the requested property.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system from which to retrieve the specified device class property. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the property is retrieved from the local system.


### -param Reserved

Reserved, must be <b>NULL</b>.


##### - Property.SPCRP_CHARACTERISTICS

The function returns flags indicating device characteristics for the class. For a list of characteristics flags, see the <i>DeviceCharacteristics</i> parameter to <a href="https://msdn.microsoft.com/library/windows/hardware/ff548397">IoCreateDevice</a>.


##### - Property.SPCRP_DEVTYPE

The function returns a DWORD value that represents the device type for the class. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563821">Specifying Device Types</a>.


##### - Property.SPCRP_EXCLUSIVE

The function returns a DWORD value indicating whether users can obtain exclusive access to devices for this class. The returned value is one if exclusive access is allowed, or zero otherwise.


##### - Property.SPCRP_LOWERFILTERS

(Windows Vista and later) The function returns a REG_MULTI_SZ list of the service names of the lower filter drivers that are installed for the device setup class.


##### - Property.SPCRP_SECURITY

The function returns the device's security descriptor as a SECURITY_DESCRIPTOR structure in self-relative format (described in the Microsoft Windows SDK documentation).


##### - Property.SPCRP_SECURITY_SDS

The function returns the device's security descriptor as a text string. For information about security descriptor strings, see <a href="https://msdn.microsoft.com/2b15325e-34ed-497b-ae6d-3ec3ac168232">Security Descriptor Definition Language (Windows)</a>. For information about the format of security descriptor strings, see Security Descriptor Definition Language (Windows).


##### - Property.SPCRP_UPPERFILTERS

(Windows Vista and later) The function returns a REG_MULTI_SZ list of the service names of the upper filter drivers that are installed for the device setup class.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552135">SetupDiSetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552169">SetupDiSetDeviceRegistryProperty</a>
 

 

