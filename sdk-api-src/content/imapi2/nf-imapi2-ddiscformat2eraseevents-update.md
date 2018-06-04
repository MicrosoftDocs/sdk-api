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

# DDiscFormat2EraseEvents::Update


## -description


Implement this method to receive progress notification of the current erase operation.


## -parameters




### -param object [in]

The <a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a> interface that initiated the erase operation. 

This parameter is a <b>MsftDiscFormat2Erase</b> object in script.


### -param elapsedSeconds [in]

Elapsed time, in seconds, of the erase operation. 


### -param estimatedTotalSeconds [in]

Estimated time, in seconds, to complete the erase operation. 


## -returns



Return values are ignored.




## -remarks



Notifications are sent in response to calling the <a href="https://msdn.microsoft.com/dc71d1bf-b068-42c0-a87d-ae8fac279a58">IDiscFormat2Erase::EraseMedia</a> method. 

Notification is sent every 0.5 or 1.0 seconds depending on the method required to blank the media.

Total time estimates for a single erasure can vary as the operation progresses. The drive provides updated information that can affect the projected duration of the erasure.




## -see-also




<a href="https://msdn.microsoft.com/0e999859-d409-4fd8-a5da-c43da64bcd8f">DDiscFormat2EraseEvents</a>
 

 

