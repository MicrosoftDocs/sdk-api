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

# tagOFFLINEFILES_CACHING_MODE enumeration


## -description


Describes the caching mode used in methods such as <a href="https://msdn.microsoft.com/4d9a2fda-baad-4ada-8a07-f39c9cfafdfa">IOfflineFilesCache::IsPathCacheable</a> and <a href="https://msdn.microsoft.com/0045497b-0f90-4e20-80c9-6b74e4b523b8">IOfflineFilesShareInfo::GetShareCachingMode</a>.


## -enum-fields




### -field OFFLINEFILES_CACHING_MODE_NONE

No caching mode value was found.


### -field OFFLINEFILES_CACHING_MODE_NOCACHING

The share or shared folder is configured to disallow caching.


### -field OFFLINEFILES_CACHING_MODE_MANUAL

The share or shared folder is configured to allow manual caching.


### -field OFFLINEFILES_CACHING_MODE_AUTO_DOC

The share or shared folder is configured to allow automatic caching of documents.


### -field OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC

The share or shared folder is configured to allow automatic caching of programs and documents.


## -see-also




<a href="https://msdn.microsoft.com/4d9a2fda-baad-4ada-8a07-f39c9cfafdfa">IOfflineFilesCache::IsPathCacheable</a>



<a href="https://msdn.microsoft.com/0045497b-0f90-4e20-80c9-6b74e4b523b8">IOfflineFilesShareInfo::GetShareCachingMode</a>



<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a>
 

 

