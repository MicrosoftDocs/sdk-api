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

# _BG_JOB_REPLY_PROGRESS structure


## -description


The 
<b>BG_JOB_REPLY_PROGRESS</b> structure provides progress information related to the reply portion of an upload-reply job.


## -struct-fields




### -field BytesTotal

Size of the file in bytes. The value is <b>BG_SIZE_UNKNOWN</b> if the reply has not begun.


### -field BytesTransferred

Number of bytes transferred.


## -see-also




<a href="https://msdn.microsoft.com/76509b1a-fdfb-4236-8554-f63282bfc1b6">IBackgroundCopyJob2::GetReplyProgress</a>
 

 

