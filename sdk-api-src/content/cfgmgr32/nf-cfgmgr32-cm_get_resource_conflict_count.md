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

# CM_Get_Resource_Conflict_Count function


## -description


The <b>CM_Get_Resource_Conflict_Count</b> function obtains the number of conflicts contained in a specified resource conflict list.


## -parameters




### -param clConflictList [in]

Caller-supplied handle to a conflict list, obtained by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.


### -param pulCount [out]

Caller-supplied address of a location to receive the conflict count.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The count value obtained by calling <b>CM_Get_Resource_Conflict_Count</b> can be used to determine the number of times to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538631">CM_Get_Resource_Conflict_Details</a>, which supplies information about each conflict.

If there are no entries in the conflict list, the location supplied by <i>pulCount</i> will receive zero.



