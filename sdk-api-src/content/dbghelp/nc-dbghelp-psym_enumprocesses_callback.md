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

# PSYM_ENUMPROCESSES_CALLBACK callback function


## -description


An application-defined function used with the <a href="https://msdn.microsoft.com/281b83ff-8375-4edb-8a10-97af5dbdc87b">SymEnumProcesses</a> function.

The <b>PSYM_ENUMPROCESSES_CALLBACK</b> type defines a pointer to this callback function. 
<b>SymEnumProcessesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param hProcess [in]

A handle to the process.


### -param UserContext [in]

The user-defined value passed from the 
<a href="https://msdn.microsoft.com/281b83ff-8375-4edb-8a10-97af5dbdc87b">SymEnumProcesses</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns




						If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://msdn.microsoft.com/281b83ff-8375-4edb-8a10-97af5dbdc87b">SymEnumProcesses</a>
 

 

