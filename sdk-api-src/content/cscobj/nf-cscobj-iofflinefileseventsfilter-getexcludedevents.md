---
UID: NF:cscobj.IOfflineFilesEventsFilter.GetExcludedEvents
title: IOfflineFilesEventsFilter::GetExcludedEvents
author: windows-sdk-content
description: Retrieves an array of OFFLINEFILES_EVENTS enumeration values describing which events should not be received by the event sink.
old-location: of\iofflinefileseventsfilter_getexcludedevents.htm
tech.root: offlinefiles
ms.assetid: 40e388b2-b051-4b0a-b96e-7a73b521758e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetExcludedEvents, GetExcludedEvents method [Offline Files], GetExcludedEvents method [Offline Files],IOfflineFilesEventsFilter interface, IOfflineFilesEventsFilter interface [Offline Files],GetExcludedEvents method, IOfflineFilesEventsFilter.GetExcludedEvents, IOfflineFilesEventsFilter::GetExcludedEvents, cscobj/IOfflineFilesEventsFilter::GetExcludedEvents, of.iofflinefileseventsfilter_getexcludedevents
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
 - IOfflineFilesEventsFilter.GetExcludedEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEventsFilter::GetExcludedEvents


## -description


Retrieves an array of <a href="https://msdn.microsoft.com/en-us/library/Bb530645(v=VS.85).aspx">OFFLINEFILES_EVENTS</a> enumeration values describing which events should not be received by the event sink. If a particular event is specified both in <a href="https://msdn.microsoft.com/en-us/library/Bb530535(v=VS.85).aspx">IOfflineFilesEventsFilter::GetIncludedEvents</a> and <b>IOfflineFilesEventsFilter::GetExcludedEvents</b>, the event is excluded from this event sink.


## -parameters




### -param cElements [in]

Specifies the maximum number of elements that can be stored in the array referenced by the <i>prgEvents</i> parameter.


### -param prgEvents [out]

Contains the address of an array of <a href="https://msdn.microsoft.com/en-us/library/Bb530645(v=VS.85).aspx">OFFLINEFILES_EVENTS</a> enumeration values.  Place the <b>OFFLINEFILES_EVENT_XXXXXX</b> identifier in an array entry to specify that the corresponding event is not desired by this event sink.


### -param pcEvents [out]

Receives the actual number of elements written to the array referenced by the <i>prgEvents</i> parameter.


## -returns



Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530532(v=VS.85).aspx">IOfflineFilesEventsFilter</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530535(v=VS.85).aspx">IOfflineFilesEventsFilter::GetIncludedEvents</a>
 

 

