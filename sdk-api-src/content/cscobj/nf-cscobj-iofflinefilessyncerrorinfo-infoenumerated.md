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

# IOfflineFilesSyncErrorInfo::InfoEnumerated


## -description


Indicates whether information was queried for the local, remote, or original copy of the item during synchronization. 


## -parameters




### -param pbLocalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the local copy of the item during synchronization, or <b>FALSE</b> otherwise.


### -param pbRemoteEnumerated [out]

Receives <b>TRUE</b> if information was queried for the remote copy of the item during synchronization, or <b>FALSE</b> otherwise.


### -param pbOriginalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the original copy of the item during synchronization, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a>
 

 

