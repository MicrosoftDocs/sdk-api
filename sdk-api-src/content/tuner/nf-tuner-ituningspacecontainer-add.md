---
UID: NF:tuner.ITuningSpaceContainer.Add
title: ITuningSpaceContainer::Add (tuner.h)
author: windows-sdk-content
description: The Add method adds a new persistent tuning space to the system.
old-location: mstv\ituningspacecontainer_add.htm
tech.root: mstv
ms.assetid: 9c7faab5-48d4-47fa-be8a-7dafce8504a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],ITuningSpaceContainer interface, ITuningSpaceContainer interface [Microsoft TV Technologies],Add method, ITuningSpaceContainer.Add, ITuningSpaceContainer::Add, ITuningSpaceContainerAdd, mstv.ituningspacecontainer_add, tuner/ITuningSpaceContainer::Add
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaceContainer.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpaceContainer::Add


## -description



The <b>Add</b> method adds a new persistent tuning space to the system.




## -parameters




### -param TuningSpace [in]

Pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the new tuning space


### -param NewIndex [out]

Pointer to a variable of type <b>VARIANT</b> that receives the ID of the new tuning space within the current collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method adds a new tuning space to the collection. The collection object automatically persists the tuning space information.

The tuning space must have a unique name that does not clash with any of the tuning spaces already in the collection. To overwrite an existing tuning space, use the <a href="https://msdn.microsoft.com/44e82ec9-ffd0-4bc9-88da-b6c135cbd98f">ITuningSpaceContainer::put_Item</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

