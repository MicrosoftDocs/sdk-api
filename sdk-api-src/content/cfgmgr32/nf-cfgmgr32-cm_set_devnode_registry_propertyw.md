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

# CM_Set_DevNode_Registry_PropertyW function


## -description


The <b>CM_Set_DevNode_Registry_Property</b> function sets a specified device property in the registry.


## -parameters




### -param dnDevInst [in]

A caller-supplied device instance handle that is bound to the local machine.


### -param ulProperty [in]

A CM_DRP_-prefixed constant value that identifies the device property to be set in the registry. These constants are defined in <i>Cfgmgr32.h</i>.


### -param Buffer [in, optional]

A pointer to a caller-supplied buffer that supplies the requested device property, formatted appropriately for the property's data type. 


### -param ulLength [in]

The length, in bytes, of the supplied device property.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



For information about how to use device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538496">CM_Get_DevNode_Registry_Property</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552169">SetupDiSetDeviceRegistryProperty</a>
 

 

