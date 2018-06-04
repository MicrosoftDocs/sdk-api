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

# CM_Open_Class_KeyW function


## -description


The <b>CM_Open_Class_Key</b> function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.


## -parameters




### -param ClassGuid [in, optional]

Pointer to the GUID of the class whose registry key is to be opened. This parameter is optional and can be NULL. If this parameter is NULL, the root of the class tree is opened.


### -param pszClassName [in, optional]

Reserved. Must be set to NULL.


### -param samDesired [in]

The registry security access for the key to be opened.


### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:





#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.



#### RegDisposition_OpenExisting

Open the key only if it exists.


### -param phkClass [out]

Pointer to an HKEY that will receive the opened key upon success.


### -param ulFlags [in]

Open class key flags:





#### CM_OPEN_CLASS_KEY_INSTALLER

The key to be opened is for a device setup class.



#### CM_OPEN_CLASS_KEY_INTERFACE

The key to be opened is for a device interface class.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Close the handle returned from this function by calling <b>RegCloseKey</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537966">CM_Delete_Class_Key</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552067">SetupDiOpenClassRegKeyEx</a>
 

 

