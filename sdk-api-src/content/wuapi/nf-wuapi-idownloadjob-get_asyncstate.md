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

# IDownloadJob::get_AsyncState


## -description


Gets  the caller-specific state object that is passed to the <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> method.

This property is read-only.


## -parameters


## -remarks



This state object can be used by the caller to identify a particular download. Or, this state object can be used by the caller to pass information from the caller to the implementation of the <a href="https://msdn.microsoft.com/8fc414da-835c-438f-b607-8a273e7f9064">IDownloadProgressChangedCallback</a>  or <a href="https://msdn.microsoft.com/ad1c3075-21d9-409f-9677-fbf6d0c50313">IDownloadCompletedCallback</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a>
 

 

