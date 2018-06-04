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

# _EFFPERM_RESULT_LIST structure


## -description


The <b>EFFPERM_RESULT_LIST</b> structure lists the effective permissions.


## -struct-fields




### -field fEvaluated

Indicates if the effective permissions results have been evaluated.


### -field cObjectTypeListLength

The number of elements in both the <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members.


### -field pObjectTypeList

A pointer to an array of <a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures that specifies the properties and property sets for which access was evaluated.


### -field pGrantedAccessList

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> values that specifies the access rights granted for each corresponding object type.

