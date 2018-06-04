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

# DPA_GetPtrPtr macro


## -description


Gets the pointer to the internal pointer array of a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

A handle to an existing DPA.


## -remarks



Applications can use the return value to manipulate the contents of the DPA directly instead of using functions such as <a href="https://msdn.microsoft.com/3ba855f8-e077-4886-b2fc-002515242dd3">DPA_SetPtr</a>. The return value is invalidated by any operation that changes the number of elements in the DPA or destroys the DPA. 
For example, after calling function <a href="https://msdn.microsoft.com/275585f9-b26b-4528-a5b2-471dc1623a68">DPA_InsertPtr</a> on a DPA, any internal pointers retrieved by calling the macro <b>DPA_GetPtrPtr</b> on the same DPA are no longer valid.



