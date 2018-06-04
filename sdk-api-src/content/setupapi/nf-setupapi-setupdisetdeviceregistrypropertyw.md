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

# SetupDiSetDeviceRegistryPropertyW function


## -description


The <b>SetupDiSetDeviceRegistryProperty</b> function sets a Plug and Play device property for a device.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to set a Plug and Play device property.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. If the <b>ClassGuid</b> property is set, <i>DeviceInfoData.</i><b>ClassGuid</b> is set upon return to the new class for the device.


### -param Property [in]

One of the following values, which identifies the property to be set. For descriptions of these values, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a>. 

<div class="alert"><b>Note</b>  <b>SPDRP_HARDWAREID</b> or <b>SPDRP_COMPATIBLEIDS</b> can only be used when <i>DeviceInfoData</i> represents a root-enumerated device. For other devices, the bus driver reports hardware and compatible IDs when enumerating a child device after receiving <a href="https://msdn.microsoft.com/library/windows/hardware/ff551679">IRP_MN_QUERY_ID</a>.</div>
<div> </div>
The following values are reserved for use by the operating system and cannot be used in the <i>Property</i> parameter:


### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the new data for the property. If the property is being cleared, then this pointer should be <b>NULL</b> and <i>PropertyBufferSize</i> must be zero.


### -param PropertyBufferSize [in]

The size, in bytes, of <i>PropertyBuffer</i>. If <i>PropertyBuffer</i> is <b>NULL</b>, then this field must be zero.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

The class name property cannot be set because it is based on the corresponding class GUID and is automatically updated when that property is changed. When the ClassGUID property changes, <b>SetupDiSetDeviceRegistryProperty</b> automatically cleans up any software keys associated with the device.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551097">SetupDiGetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552135">SetupDiSetClassRegistryProperty</a>
 

 

