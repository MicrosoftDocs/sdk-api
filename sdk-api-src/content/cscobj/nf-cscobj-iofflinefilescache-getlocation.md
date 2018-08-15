---
UID: NF:cscobj.IOfflineFilesCache.GetLocation
title: IOfflineFilesCache::GetLocation
author: windows-sdk-content
description: Retrieves the current fully qualified directory path of the Offline Files cache.
old-location: of\iofflinefilescache_getlocation.htm
old-project: offlinefiles
ms.assetid: e608c662-23d2-4dcc-95fc-e949ba9f848f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLocation, GetLocation method [Offline Files], GetLocation method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetLocation method, IOfflineFilesCache.GetLocation, IOfflineFilesCache::GetLocation, cscobj/IOfflineFilesCache::GetLocation, of.iofflinefilescache_getlocation
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
 - IOfflineFilesCache.GetLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache::GetLocation


## -description


Retrieves the current fully qualified directory path of the Offline Files cache.


## -parameters




### -param ppszPath [out]

Address of pointer variable to accept the address of a string containing the fully qualified path of the Offline Files cache directory.  Upon successful return, the caller is expected to free the returned buffer by using  the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

