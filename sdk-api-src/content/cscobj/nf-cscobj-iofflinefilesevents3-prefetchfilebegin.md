---
UID: NF:cscobj.IOfflineFilesEvents3.PrefetchFileBegin
title: IOfflineFilesEvents3::PrefetchFileBegin
author: windows-sdk-content
description: Reports that a file prefetch operation has begun.
old-location: of\iofflinefilesevents3_prefetchfilebegin.htm
old-project: offlinefiles
ms.assetid: b65354ed-dc4b-491c-9672-2f5fa91093bd
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IOfflineFilesEvents3 interface [Offline Files],PrefetchFileBegin method, IOfflineFilesEvents3.PrefetchFileBegin, IOfflineFilesEvents3::PrefetchFileBegin, PrefetchFileBegin, PrefetchFileBegin method [Offline Files], PrefetchFileBegin method [Offline Files],IOfflineFilesEvents3 interface, cscobj/IOfflineFilesEvents3::PrefetchFileBegin, of.iofflinefilesevents3_prefetchfilebegin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - IOfflineFilesEvents3.PrefetchFileBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents3::PrefetchFileBegin


## -description


Reports that a file prefetch operation has begun.


## -parameters




### -param pszPath [in]

The UNC path of the file.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/f68c2c0c-e4f7-4048-99c9-761f98928157">IOfflineFilesEvents3</a>
 

 

