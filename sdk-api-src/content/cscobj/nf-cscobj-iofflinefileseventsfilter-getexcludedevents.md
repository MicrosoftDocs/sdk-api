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

# IOfflineFilesEventsFilter::GetExcludedEvents


## -description



    Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should not be received by the event sink. If a particular event is specified both in <a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">IOfflineFilesEventsFilter::GetIncludedEvents</a> and <b>IOfflineFilesEventsFilter::GetExcludedEvents</b>, the event is excluded from this event sink.


## -parameters




### -param cElements [in]

Specifies the maximum number of elements that can be stored in the array referenced by the <i>prgEvents</i> parameter.


### -param prgEvents [out]

Contains the address of an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values.  Place the <b>OFFLINEFILES_EVENT_XXXXXX</b> identifier in an array entry to specify that the corresponding event is not desired by this event sink.


### -param pcEvents [out]

Receives the actual number of elements written to the array referenced by the <i>prgEvents</i> parameter.


## -returns



Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.




## -see-also




<a href="https://msdn.microsoft.com/8c2c793e-c91c-4ca7-a03c-e349de00de6c">IOfflineFilesEventsFilter</a>



<a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">IOfflineFilesEventsFilter::GetIncludedEvents</a>
 

 

