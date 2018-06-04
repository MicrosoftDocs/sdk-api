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

# LSA_FOREST_TRUST_COLLISION_RECORD_TYPE enumeration


## -description


The <b>LSA_FOREST_TRUST_COLLISION_RECORD_TYPE</b> enumeration defines the types of collision that can occur between <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust records.


## -enum-fields




### -field CollisionTdo

Collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects. This indicates a collision with a namespace element of another forest.


### -field CollisionXref

Collision between cross-references. This indicates a collision with a domain in the same forest.


### -field CollisionOther

Collision that is not a collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects or cross-references.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/9f9d2f57-0e7f-4222-be35-e3f026b60e93">LSA_FOREST_TRUST_COLLISION_RECORD</a> structure.



