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

# CM_Delete_Class_Key function


## -description


The <b>CM_Delete_Class_Key</b> function removes the specified installed <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device class</a> from the system.


## -parameters




### -param ClassGuid [in]

Pointer to the GUID of the device class to remove.


### -param ulFlags [in]

Delete class key flags:





#### CM_DELETE_CLASS_ONLY

Delete the class only if it does not contain any subkeys.



#### CM_DELETE_CLASS_SUBKEYS

Delete the class and all of its subkeys.



#### CM_DELETE_CLASS_INTERFACE (available only in Windows Vista and later)

Indicates that <i>ClassGuid</i> specifies a <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> and not a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538806">CM_Open_Class_Key</a>
 

 

