---
UID: NF:imapi2.DDiscFormat2EraseEvents.Update
title: DDiscFormat2EraseEvents::Update
author: windows-sdk-content
description: Implement this method to receive progress notification of the current erase operation.
old-location: imapi\ddiscformat2eraseevents_update.htm
tech.root: imapi
ms.assetid: 9cb52a79-84cf-49e5-a6b8-7baacb403ce9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DDiscFormat2EraseEvents interface [IMAPI],Update method, DDiscFormat2EraseEvents.Update, DDiscFormat2EraseEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2EraseEvents interface, imapi.ddiscformat2eraseevents_update, imapi2/DDiscFormat2EraseEvents::Update
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2EraseEvents.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

