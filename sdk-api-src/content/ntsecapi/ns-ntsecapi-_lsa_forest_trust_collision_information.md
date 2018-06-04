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

# _LSA_FOREST_TRUST_COLLISION_INFORMATION structure


## -description


The <b>LSA_FOREST_TRUST_COLLISION_INFORMATION</b> structure contains information about <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust collisions.


## -struct-fields




### -field RecordCount

Number of <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures in the array pointed to by the <b>Entries</b> member.


### -field Entries

Pointer to a pointer to an array of <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structures, each of which contains information about a single collision.


### -field Entries.size_is

 


### -field Entries.size_is.RecordCount

 



