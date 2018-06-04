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

# GROUP_FAILURE_INFO_BUFFER structure


## -description


Represents a buffer for a <a href="https://msdn.microsoft.com/C3E7585B-21F8-4E4C-A970-C07F72C80E76">GROUP_FAILURE_INFO</a> structure.


## -struct-fields




### -field dwVersion

The version of this structure. Set this parameter to <b>GROUP_FAILURE_INFO_VERSION_1</b>        (0x1).


### -field Info

The <a href="https://msdn.microsoft.com/C3E7585B-21F8-4E4C-A970-C07F72C80E76">GROUP_FAILURE_INFO</a> structure that contains information about the failover attempts for the group failure.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

