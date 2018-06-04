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

# DsMergeForestTrustInformationW function


## -description


The <b>DsMergeForestTrustInformationW</b> function merges the changes from a new forest trust data structure with an old forest trust data structure.


## -parameters




### -param DomainName [in]

Pointer to a null-terminated Unicode string that specifies the trusted domain to  update.


### -param NewForestTrustInfo [in]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure that contains the new forest trust data to be merged.
        The <b>Flags</b> and <b>Time</b> members of the entries are ignored.


### -param OPTIONAL

TBD


### -param MergedForestTrustInfo

TBD




#### - ForestTrustInfo [out]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure pointer that receives the merged forest trust data.

The caller must free this structure when it is no longer required by calling <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>.


#### - OldForestTrustInfo [in, optional]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure that contains the old forest trust data to be merged.
        This parameter may be <b>NULL</b> if no records exist.


## -returns



Returns <b>NO_ERROR</b> if successful or a Windows error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 

