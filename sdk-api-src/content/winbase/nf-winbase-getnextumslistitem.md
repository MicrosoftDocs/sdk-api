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

# GetNextUmsListItem function


## -description


Returns the next user-mode scheduling (UMS) thread context in a list of thread contexts.


## -parameters




### -param UmsContext [in, out]

A pointer to a UMS context in a list of thread contexts. This list is retrieved by the <a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a> function. 


## -returns



If the function succeeds, it returns a pointer to the next thread context in the list.

If there is no thread context after the context specified by the <i>UmsContext</i> parameter,  the function returns NULL. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>
 

 

