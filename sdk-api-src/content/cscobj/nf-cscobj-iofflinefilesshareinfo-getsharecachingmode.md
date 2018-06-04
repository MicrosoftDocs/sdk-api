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

# IOfflineFilesShareInfo::GetShareCachingMode


## -description


Retrieves the caching mode configuration of the closest ancestor share to the item.


## -parameters




### -param pCachingMode [out]

Receives a value from the <a href="https://msdn.microsoft.com/833cd194-7086-4faa-a05b-5f8beda62f0a">OFFLINEFILES_CACHING_MODE</a> enumeration that indicates the caching mode.

The following values can be returned:



#### OFFLINEFILES_CACHING_MODE_NONE (0)

No caching mode value was found. This value can be returned if the method fails.



#### OFFLINEFILES_CACHING_MODE_NOCACHING (1)

The share is configured to disallow caching. This value corresponds to a value of zero returned by the <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_MANUAL (2)

The share is configured to allow manual caching. This value corresponds to a value of <b>CSC_CACHE_MANUAL_REINT</b> returned by the <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> function for the CSC_MASK portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_AUTO_DOC (3)

The share is configured to allow automatic caching of documents. This value corresponds to a value of <b>CSC_CACHE_AUTO_REINT</b> returned by the <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC (4)

The share is configured to allow automatic caching of programs and documents. This value corresponds to a value of <b>CSC_CACHE_VDO</b> (virtual disconnected operations) returned by the <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method is equivalent to locating the nearest share item, obtaining its fully qualified UNC path and calling <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> for <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> information.




## -see-also




<a href="https://msdn.microsoft.com/4d9a2fda-baad-4ada-8a07-f39c9cfafdfa">IOfflineFilesCache::IsPathCacheable</a>



<a href="https://msdn.microsoft.com/9647aae3-06ca-4813-8243-3d0fb794802d">IOfflineFilesShareInfo</a>
 

 

