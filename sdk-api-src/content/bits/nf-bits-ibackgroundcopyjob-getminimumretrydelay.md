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

# IBackgroundCopyJob::GetMinimumRetryDelay


## -description


Retrieves the minimum length of time that the service waits after encountering a transient error condition before trying to transfer the file.


## -parameters




### -param Seconds






#### - pRetryDelay [in]

Length of time, in seconds, that the service waits after encountering a transient error before trying to transfer the file.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/4881e5f7-a835-40d5-a056-d6b23e3cd84c">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">IBackgroundCopyJob::SetMinimumRetryDelay</a>
 

 

