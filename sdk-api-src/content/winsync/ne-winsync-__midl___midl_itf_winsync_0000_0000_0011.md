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

# __MIDL___MIDL_itf_winsync_0000_0000_0011 enumeration


## -description


Represents the possible results when a knowledge cookie is compared with a knowledge object by using <a href="https://msdn.microsoft.com/f1649f70-8c8b-4eea-8ecb-7ea5a657eabe">ISyncKnowledge2::CompareToKnowledgeCookie</a>.


## -enum-fields




### -field KCCR_COOKIE_KNOWLEDGE_EQUAL

The knowledge cookie is equal to the specified knowledge.


### -field KCCR_COOKIE_KNOWLEDGE_CONTAINED

The knowledge cookie is contained by the specified knowledge.


### -field KCCR_COOKIE_KNOWLEDGE_CONTAINS

The knowledge cookie contains the specified knowledge.


### -field KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE

The knowledge cookie cannot be compared to the specified knowledge.


## -remarks



A knowledge cookie is a lightweight, read-only representation of knowledge that can be used for fast comparisons when performance is especially important.




## -see-also




<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>



<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

