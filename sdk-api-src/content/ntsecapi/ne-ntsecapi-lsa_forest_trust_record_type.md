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

# LSA_FOREST_TRUST_RECORD_TYPE enumeration


## -description


The <b>LSA_FOREST_TRUST_RECORD_TYPE</b> enumeration defines the type of a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust record.


## -enum-fields




### -field ForestTrustTopLevelName

Record contains an included top-level name.


### -field ForestTrustTopLevelNameEx

Record contains an excluded top-level name.


### -field ForestTrustDomainInfo

Record contains an <a href="https://msdn.microsoft.com/c0e06735-ca10-4bee-a45b-6db5b6666e31">LSA_FOREST_TRUST_DOMAIN_INFO</a> structure.


### -field ForestTrustRecordTypeLast

Marks the end of an enumeration.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/19b4ee56-664f-4f37-bfc9-129032ebeb22">LSA_FOREST_TRUST_RECORD</a> structure.



