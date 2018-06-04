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

# ITuningSpaceContainer::Add


## -description



The <b>Add</b> method adds a new persistent tuning space to the system.




## -parameters




### -param TuningSpace




### -param NewIndex






#### - pNewIndex [out]

Pointer to a variable of type <b>VARIANT</b> that receives the ID of the new tuning space within the current collection.


#### - pTuningSpace [in]

Pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the new tuning space


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method adds a new tuning space to the collection. The collection object automatically persists the tuning space information.

The tuning space must have a unique name that does not clash with any of the tuning spaces already in the collection. To overwrite an existing tuning space, use the <a href="https://msdn.microsoft.com/44e82ec9-ffd0-4bc9-88da-b6c135cbd98f">ITuningSpaceContainer::put_Item</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

