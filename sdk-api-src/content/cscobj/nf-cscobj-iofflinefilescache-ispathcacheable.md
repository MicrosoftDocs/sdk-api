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

# IOfflineFilesCache::IsPathCacheable


## -description



    Determines whether a specified UNC path is in the Offline Files cache.


## -parameters




### -param pszPath [in]

The UNC path of the item.


### -param pbCacheable [out]

Receives <b>TRUE</b> if the item is in the Offline Files cache, <b>FALSE</b> if not.


### -param pShareCachingMode [out]

Receives one of the following <a href="https://msdn.microsoft.com/833cd194-7086-4faa-a05b-5f8beda62f0a">OFFLINEFILES_CACHING_MODE</a> enumeration values indicating the caching configuration of the applicable network shared folder under which the specified item exists.



#### OFFLINEFILES_CACHING_MODE_NONE (0)

No caching mode value was found.  This value is used when the item is not cacheable or an error has occurred.



#### OFFLINEFILES_CACHING_MODE_NOCACHING (1)

The shared folder is configured to disallow caching.



#### OFFLINEFILES_CACHING_MODE_MANUAL (2)

The shared folder is configured to allow manual caching.



#### OFFLINEFILES_CACHING_MODE_AUTO_DOC (3)

The shared folder is configured to allow automatic caching of documents.



#### OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC (4)

The shared folder is configured to allow automatic caching of programs and documents.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The caching mode value returned is equivalent to the <b>CSC_MASK</b> value associated with <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> returned by <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>.  The value mapping is as follows:

<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/833cd194-7086-4faa-a05b-5f8beda62f0a">OFFLINEFILES_CACHING_MODE</a> Value</th>
<th>
<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> Value</th>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_NOCACHING</b></td>
<td>0</td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_MANUAL</b></td>
<td><b>CSC_CACHE_MANUAL_REINT</b></td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_AUTO_DOC</b></td>
<td><b>CSC_CACHE_AUTO_REINT</b></td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC</b></td>
<td><b>CSC_CACHE_VDO</b></td>
</tr>
</table>
 

These settings are configured as attributes of the shared folder on the server by clicking the Caching button on the shared folder's Sharing property page or by using the <code>net share /cache</code> command.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>



<a href="https://msdn.microsoft.com/0045497b-0f90-4e20-80c9-6b74e4b523b8">IOfflineFilesShareInfo::GetShareCachingMode</a>



<a href="https://msdn.microsoft.com/833cd194-7086-4faa-a05b-5f8beda62f0a">OFFLINEFILES_CACHING_MODE</a>
 

 

