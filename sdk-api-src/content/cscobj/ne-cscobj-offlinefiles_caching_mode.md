---
UID: NE:cscobj.tagOFFLINEFILES_CACHING_MODE
title: OFFLINEFILES_CACHING_MODE (cscobj.h)
author: windows-sdk-content
description: Describes the caching mode used in methods such as IOfflineFilesCache::IsPathCacheable and IOfflineFilesShareInfo::GetShareCachingMode.
old-location: of\offlinefiles_caching_mode.htm
tech.root: offlinefiles
ms.assetid: 833cd194-7086-4faa-a05b-5f8beda62f0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_CACHING_MODE, OFFLINEFILES_CACHING_MODE enumeration [Offline Files], OFFLINEFILES_CACHING_MODE_AUTO_DOC, OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, OFFLINEFILES_CACHING_MODE_MANUAL, OFFLINEFILES_CACHING_MODE_NOCACHING, OFFLINEFILES_CACHING_MODE_NONE, cscobj/OFFLINEFILES_CACHING_MODE, cscobj/OFFLINEFILES_CACHING_MODE_AUTO_DOC, cscobj/OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, cscobj/OFFLINEFILES_CACHING_MODE_MANUAL, cscobj/OFFLINEFILES_CACHING_MODE_NOCACHING, cscobj/OFFLINEFILES_CACHING_MODE_NONE, of.offlinefiles_caching_mode
ms.topic: enum
req.header: cscobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_CACHING_MODE
product: Windows
targetos: Windows
req.typenames: OFFLINEFILES_CACHING_MODE
req.redist: 
ms.custom: 19H1
---

# OFFLINEFILES_CACHING_MODE enumeration


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
 

 

