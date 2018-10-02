---
UID: NF:cscobj.IOfflineFilesEventsFilter.GetPathFilter
title: IOfflineFilesEventsFilter::GetPathFilter
author: windows-sdk-content
description: Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.
old-location: of\iofflinefileseventsfilter_getpathfilter.htm
tech.root: OfflineFiles
ms.assetid: 0b9d8339-3daa-4f0c-8a52-59e06b663163
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPathFilter, GetPathFilter method [Offline Files], GetPathFilter method [Offline Files],IOfflineFilesEventsFilter interface, IOfflineFilesEventsFilter interface [Offline Files],GetPathFilter method, IOfflineFilesEventsFilter.GetPathFilter, IOfflineFilesEventsFilter::GetPathFilter, cscobj/IOfflineFilesEventsFilter::GetPathFilter, of.iofflinefileseventsfilter_getpathfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IOfflineFilesEventsFilter.GetPathFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEventsFilter::GetPathFilter


## -description


Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.


## -parameters




### -param ppszFilter [out]

Receives a fully qualified UNC path string identifying the path associated with the filter. The memory for this string must be allocated using the <a href="https://msdn.microsoft.com/en-us/library/ms692727(v=VS.85).aspx">CoTaskMemAlloc</a> function.


### -param pMatch [out]

Receives an <a href="https://msdn.microsoft.com/en-us/library/Bb530651(v=VS.85).aspx">OFFLINEFILES_PATHFILTER_MATCH</a> enumeration  value indicating which descendants of the filter path are to be included in the set of events delivered to the event sink.


## -returns



Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530532(v=VS.85).aspx">IOfflineFilesEventsFilter</a>
 

 

