---
UID: NF:cscobj.IOfflineFilesShareInfo.GetShareCachingMode
title: IOfflineFilesShareInfo::GetShareCachingMode
author: windows-sdk-content
description: Retrieves the caching mode configuration of the closest ancestor share to the item.
old-location: of\iofflinefilesshareinfo_getsharecachingmode.htm
old-project: offlinefiles
ms.assetid: 0045497b-0f90-4e20-80c9-6b74e4b523b8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetShareCachingMode, GetShareCachingMode method [Offline Files], GetShareCachingMode method [Offline Files],IOfflineFilesShareInfo interface, IOfflineFilesShareInfo interface [Offline Files],GetShareCachingMode method, IOfflineFilesShareInfo.GetShareCachingMode, IOfflineFilesShareInfo::GetShareCachingMode, OFFLINEFILES_CACHING_MODE_AUTO_DOC, OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, OFFLINEFILES_CACHING_MODE_MANUAL, OFFLINEFILES_CACHING_MODE_NOCACHING, OFFLINEFILES_CACHING_MODE_NONE, cscobj/IOfflineFilesShareInfo::GetShareCachingMode, of.iofflinefilesshareinfo_getsharecachingmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesShareInfo.GetShareCachingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
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

The share is configured to allow automatic caching of documents. This value corresponds to a value of <b>CSC_CACHE_AUTO_REINT</b> returned by the <a href="https://msdn.microsoft.com/en-us/library/Bb525388(v=VS.85).aspx">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.



#### OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC (4)

The share is configured to allow automatic caching of programs and documents. This value corresponds to a value of <b>CSC_CACHE_VDO</b> (virtual disconnected operations) returned by the <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> function for the <b>CSC_MASK</b> portion of the <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method is equivalent to locating the nearest share item, obtaining its fully qualified UNC path and calling <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> for <a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> information.




## -see-also




<a href="https://msdn.microsoft.com/4d9a2fda-baad-4ada-8a07-f39c9cfafdfa">IOfflineFilesCache::IsPathCacheable</a>



<a href="https://msdn.microsoft.com/9647aae3-06ca-4813-8243-3d0fb794802d">IOfflineFilesShareInfo</a>
 

 

