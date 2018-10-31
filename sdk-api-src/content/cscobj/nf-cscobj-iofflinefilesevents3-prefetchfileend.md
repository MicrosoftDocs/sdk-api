---
UID: NF:cscobj.IOfflineFilesEvents3.PrefetchFileEnd
title: IOfflineFilesEvents3::PrefetchFileEnd
author: windows-sdk-content
description: Reports that a file prefetch operation has ended.
old-location: of\iofflinefilesevents3_prefetchfileend.htm
tech.root: OfflineFiles
ms.assetid: d5370d39-dd66-49c1-8774-cf335aa88e96
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesEvents3 interface [Offline Files],PrefetchFileEnd method, IOfflineFilesEvents3.PrefetchFileEnd, IOfflineFilesEvents3::PrefetchFileEnd, PrefetchFileEnd, PrefetchFileEnd method [Offline Files], PrefetchFileEnd method [Offline Files],IOfflineFilesEvents3 interface, cscobj/IOfflineFilesEvents3::PrefetchFileEnd, of.iofflinefilesevents3_prefetchfileend
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents3.PrefetchFileEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents3::PrefetchFileEnd


## -description


Reports that a file prefetch operation has ended.


## -parameters




### -param pszPath [in]

The UNC path of the file.


### -param hrResult [in]

Receives the result of the operation. Contains <b>S_OK</b> if the operation completed successfully or an error value otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/f68c2c0c-e4f7-4048-99c9-761f98928157">IOfflineFilesEvents3</a>
 

 

