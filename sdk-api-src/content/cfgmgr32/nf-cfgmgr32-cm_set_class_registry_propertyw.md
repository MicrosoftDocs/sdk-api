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

# CM_Set_Class_Registry_PropertyW function


## -description


The <b>CM_Set_Class_Registry_Property</b> function sets or deletes a property of a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a>.


## -parameters




### -param ClassGuid [in]

A pointer to the GUID that represents the device setup class for which to set a property.


### -param ulProperty [in]

A value of type ULONG that identifies the property to set. This value must be one of the CM_CRP_<i>Xxx</i> values that are described for the <i>ulProperty</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538098">CM_Get_Class_Registry_Property</a> function.


### -param Buffer [in, optional]

A pointer to a buffer that contains the property data. This parameter is optional and can be set to <b>NULL</b>. For more information about setting this parameter and the corresponding <i>ulLength</i> parameter, see the following <b>Remarks</b> section.


### -param ulLength [in]

A value of type ULONG that specifies the size, in bytes, of the property data. 


### -param ulFlags [in]

Reserved for internal use only. Must be set to zero.


### -param hMachine [in, optional]

A handle to a remote machine on which to set the specified <a href="devinst.accessing_device_setup_class_properties">device setup class property</a>. This parameter is optional. If set to <b>NULL</b>, the property is set on the local machine.


## -returns



If the operation succeeds, <b>CM_Set_Class_Registry_Property </b>returns CR_SUCCESS. Otherwise, the function returns one of the other CR_<i>Xxx</i> status codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



If <i>Buffer</i> is <b>NULL</b>, <i>ulLength</i> must be set to zero.

If <i>ulLength</i> is set to zero, the function deletes the property. 

If <i>Buffer</i> is not set to <b>NULL</b> and <i>ulLength</i> is not set to zero, the supplied value must be the correct size for the REG_<i>Xxx</i> data type for the property that is specified in <i>ulProperty</i>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538098">CM_Get_Class_Registry_Property</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551097">SetupDiGetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552135">SetupDiSetClassRegistryProperty</a>
 

 

