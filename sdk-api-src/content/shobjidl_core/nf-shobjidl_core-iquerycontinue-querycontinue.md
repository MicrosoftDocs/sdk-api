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

# IQueryContinue::QueryContinue


## -description


Returns <b>S_OK</b> if the operation associated with the current instance of this interface should continue.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the calling application should continue, <b>S_FALSE</b> if not.




## -remarks



In typical usage, a pointer to an <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a> interface is passed to a method of another object.	That object, in turn, runs this method periodically to determine whether to continue its actions. For example, if a user clicks a cancel button, this method will start returning <b>S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a>



<a href="https://msdn.microsoft.com/24ff171c-e9e2-4d62-8a8c-d62e5d7a92ad">IUserNotification</a>
 

 

