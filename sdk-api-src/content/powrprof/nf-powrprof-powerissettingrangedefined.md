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

# PowerIsSettingRangeDefined function


## -description


Queries whether the specified power setting represents a range of possible values.


## -parameters




### -param OPTIONAL

TBD




#### - SettingGuid [in, optional]

The identifier of the power setting to query.


#### - SubKeyGuid [in, optional]

The identifier of the subkey to search.


## -returns



TRUE if the registry key specified by <i>SubKeyGuid</i> represents a single power setting. 

If the registry key specified by <i>SubKeyGuid</i>  represents a range, this function returns FALSE.



