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

# IDownloadProgressChangedCallback::Invoke


## -description


Handles the notification of a change in the progress of an asynchronous download that was initiated by calling the <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> method.


## -parameters




### -param downloadJob [in]

An <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface that contains download information.


### -param callbackArgs [in]

An <a href="https://msdn.microsoft.com/014bb208-1241-4022-b37a-cd16da48174c">IDownloadProgressChangedCallbackArgs</a> interface that contains download progress data.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns   a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/8fc414da-835c-438f-b607-8a273e7f9064">IDownloadProgressChangedCallback</a>



<a href="https://msdn.microsoft.com/09bdbb3a-0556-4b3a-ba18-2fe7bcb33999">IUpdateDownloader::BeginDownload</a>
 

 

