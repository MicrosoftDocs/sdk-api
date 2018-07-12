---
UID: NF:cscobj.IOfflineFilesEventsFilter.GetIncludedEvents
title: IOfflineFilesEventsFilter::GetIncludedEvents
author: windows-sdk-content
description: Retrieves an array of OFFLINEFILES_EVENTS enumeration values describing which events should be received by the event sink.
old-location: of\iofflinefileseventsfilter_getincludedevents.htm
old-project: offlinefiles
ms.assetid: ecb10da3-7566-43f7-8349-f94e59e12907
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: GetIncludedEvents, GetIncludedEvents method [Offline Files], GetIncludedEvents method [Offline Files],IOfflineFilesEventsFilter interface, IOfflineFilesEventsFilter interface [Offline Files],GetIncludedEvents method, IOfflineFilesEventsFilter.GetIncludedEvents, IOfflineFilesEventsFilter::GetIncludedEvents, cscobj/IOfflineFilesEventsFilter::GetIncludedEvents, of.iofflinefileseventsfilter_getincludedevents
ms.prod: windows
ms.technology: windows-sdk
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
 - IOfflineFilesEventsFilter.GetIncludedEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEventsFilter::GetIncludedEvents


## -description


Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should be received by the event sink. If a particular event is specified both in <b>IOfflineFilesEventsFilter::GetIncludedEvents</b> and <a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">IOfflineFilesEventsFilter::GetExcludedEvents</a>, the event is excluded from this event sink.


## -parameters




### -param cElements [in]

Specifies the maximum number of elements that can be stored in the array referenced by the <i>prgEvents</i> parameter.


### -param prgEvents [out]

Contains the address of an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values.  Place the <b>OFFLINEFILES_EVENT_XXXXXX</b> identifier in an array entry to specify that the corresponding event is desired by this event sink.


### -param pcEvents [out]

Receives the actual number of elements written to the array referenced by the <i>prgEvents</i> parameter.


## -returns



Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.




## -see-also




<a href="https://msdn.microsoft.com/8c2c793e-c91c-4ca7-a03c-e349de00de6c">IOfflineFilesEventsFilter</a>



<a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">IOfflineFilesEventsFilter::GetExcludedEvents</a>



<a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a>
 

 

