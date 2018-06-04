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

# __MIDL_IBackgroundCopyJob_0003 enumeration


## -description


The 
<b>BG_JOB_TYPE</b> enumeration defines constant values that specify the type of transfer job, such as download.


## -enum-fields




### -field BG_JOB_TYPE_DOWNLOAD

Specifies that the job downloads files to the client.


### -field BG_JOB_TYPE_UPLOAD

Specifies that the job uploads a file to the server. 

<b>BITS 1.2 and earlier:  </b>Not supported.


### -field BG_JOB_TYPE_UPLOAD_REPLY

Specifies that the job uploads a file to the server and receives a reply file from the server application. 

<b>BITS 1.2 and earlier:  </b>Not supported.


## -see-also




<a href="https://msdn.microsoft.com/b84c45c2-379a-40d0-91ab-0124f0ef6b00">IBackgroundCopyJob::GetType</a>



<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a>
 

 

