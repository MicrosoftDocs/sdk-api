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

# CM_Get_DevNode_Registry_PropertyW function


## -description


 The <b>CM_Get_DevNode_Registry_Property</b> function retrieves a specified device property from the registry.


## -parameters




### -param dnDevInst [in]

A caller-supplied device instance handle that is bound to the local machine.


### -param ulProperty [in]

A CM_DRP_-prefixed constant value that identifies the device property to be obtained from the registry. These constants are defined in <i>Cfgmgr32.h</i>.


### -param pulRegDataType [out, optional]

Optional, can be <b>NULL</b>. A pointer to a location that receives the registry data type, specified as a REG_-prefixed constant defined in <i>Winnt.h</i>.


### -param Buffer [out, optional]

Optional, can be <b>NULL</b>. A pointer to a caller-supplied buffer that receives the requested device property. If this value is <b>NULL</b>, the function supplies only the length of the requested data in the address pointed to by <i>pulLength</i>.


### -param pulLength [in, out]

A pointer to a ULONG variable into which the function stores the length, in bytes, of the requested device property.

If the <i>Buffer</i> parameter is set to <b>NULL</b>, the ULONG variable must be set to zero.

If the <i>Buffer</i> parameter is not set to <b>NULL</b>, the ULONG variable must be set to the length, in bytes, of the caller-supplied buffer.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



For information about how to use device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539845">CM_Set_DevNode_Registry_Property</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551967">SetupDiGetDeviceRegistryProperty</a>
 

 

