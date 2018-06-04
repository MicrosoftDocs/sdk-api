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

# DISPATCHERQUEUE_THREAD_APARTMENTTYPE enumeration


## -description


Specifies the threading apartment type for a new <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.


## -enum-fields




### -field DQTAT_COM_NONE

No COM threading apartment type specified.


### -field DQTAT_COM_ASTA

Specifies an application single-threaded apartment (ASTA) COM threading apartment.


### -field DQTAT_COM_STA

Specifies a single-threaded apartment (STA) COM threading apartment.


## -remarks



This value is relevant when <a href="https://msdn.microsoft.com/F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D">DispatcherQueueOptions.threadType</a> is  <b>DQTYPE_THREAD_DEDICATED</b>. Use <b>DQTAT_COM_NONE</b> when <b>DispatcherQueueOptions.threadType</b> is <b>DQTYPE_THREAD_CURRENT</b>.

Introduced in Windows 10, version 1709.




## -see-also




<a href="https://msdn.microsoft.com/750097BB-C4D1-4579-9353-582124D5CE3B">CreateDispatcherQueueController</a>



<a href="https://msdn.microsoft.com/F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D">DispatcherQueueOptions</a>
 

 

