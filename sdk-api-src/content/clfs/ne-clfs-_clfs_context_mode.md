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

# _CLFS_CONTEXT_MODE enumeration


## -description


Specifies a context mode type that indicates the direction and access methods  that a client uses to scan a log.  The context mode is set by using <a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>, and is embedded in the  read context that these two functions return.


## -enum-fields




### -field ClfsContextNone

Do not move the cursor.


### -field ClfsContextUndoNext

Move the cursor backward to the next undo record.


### -field ClfsContextPrevious

Move the cursor to the previous log record from the current read context.


### -field ClfsContextForward

Move the cursor to the next client log record from the current read context.


## -see-also




<a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>
 

 

