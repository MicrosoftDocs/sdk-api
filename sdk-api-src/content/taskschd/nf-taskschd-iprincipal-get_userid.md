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

# IPrincipal::get_UserId


## -description


Gets or sets the user identifier that is required to run the tasks  that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



Do not set this property if a group identifier is specified in the <a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId</a> property.

When reading or writing XML for a task, the user identifier for a principal is specified in the <a href="https://msdn.microsoft.com/7f3c92bf-c982-4155-9391-862f674a3665">UserId</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId Property of IPrincipal</a>



<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

