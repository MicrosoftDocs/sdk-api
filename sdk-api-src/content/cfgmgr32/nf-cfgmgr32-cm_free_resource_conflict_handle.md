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

# CM_Free_Resource_Conflict_Handle function


## -description


The <b>CM_Free_Resource_Conflict_Handle</b> function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.


## -parameters




### -param clConflictList [in]

Caller-supplied handle to be freed. This conflict list handle must have been previously obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



An application must call <b>CM_Free_Resource_Conflict_Handle</b> after it has finished using the handle that was obtained calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.



