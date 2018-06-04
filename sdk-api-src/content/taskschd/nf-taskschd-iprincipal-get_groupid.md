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

# IPrincipal::get_GroupId


## -description


Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



Do not set this property if a user identifier is specified in the <a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a> property.

When reading or writing XML for a task, the group identifier for a principal is specified in the <a href="https://msdn.microsoft.com/1e576c31-79a9-42d4-b497-74412e464d60">GroupId</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a>
 

 

