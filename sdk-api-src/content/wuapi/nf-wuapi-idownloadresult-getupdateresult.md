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

# IDownloadResult::GetUpdateResult


## -description


Returns an <a href="https://msdn.microsoft.com/d2a800c9-c23a-4aab-a9c6-e408349818dd">IUpdateDownloadResult</a> interface that contains the download information for a specified update.


## -parameters




### -param updateIndex [in]

The index of the update.


### -param retval [out]

An <a href="https://msdn.microsoft.com/d2a800c9-c23a-4aab-a9c6-e408349818dd">IUpdateDownloadResult</a> interface that contains the results for the specified update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns  a COM or Windows 

error code.




## -see-also




<a href="https://msdn.microsoft.com/293bea59-acec-4774-adb9-1ad1d29406c3">IDownloadResult</a>
 

 

