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

# IEnumOfflineFilesSettings::Next


## -description


Retrieves the next item in the enumeration and advances the enumerator.


## -parameters




### -param celt [in]

Number of elements requested.


### -param rgelt [out]

Array of elements returned.


### -param pceltFetched [out]

Number of elements returned.


## -returns



Returns <b>S_OK</b> if the number of elements returned is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is returned; or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2d0e45d5-5559-4c2e-9c20-4e5b84b5fbbd">IEnumOfflineFilesSettings</a>
 

 

