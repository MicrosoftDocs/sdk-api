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

# MI_Instance_ClearElement function


## -description


Clears the value of the named element (CIM property) and sets it to <b>NULL</b>.


## -parameters




### -param self [in, out]

Instance whose property will be set.


### -param name

A null-terminated string that represents the name of the property that will be cleared.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>



<a href="https://msdn.microsoft.com/1e366cc5-0fb9-41c9-961c-07b076a18529">MI_Instance_GetElement</a>



<a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a>
 

 

