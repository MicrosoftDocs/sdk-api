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

# RECORD_READING_POLICY enumeration


## -description


Specifies a hint about the order in which records are to be read from a log.


## -enum-fields




### -field RECORD_READING_POLICY_FORWARD

Indicates that records will be read in order of increasing LSN (from least recent to most recent).


### -field RECORD_READING_POLICY_BACKWARD

Indicates that records will be read in order of decreasing LSN (from most recent to least recent).


### -field RECORD_READING_POLICY_RANDOM

Indicates that records may be read in any order.



## -see-also




<a href="https://msdn.microsoft.com/a0a34300-e5de-4e47-9c61-389272283b61">ILog::SetAccessPolicyHint</a>
 

 

