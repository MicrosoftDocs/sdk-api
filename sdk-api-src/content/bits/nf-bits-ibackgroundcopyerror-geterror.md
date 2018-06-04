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

# IBackgroundCopyError::GetError


## -description


Retrieves the error code and identify the context in which the error occurred.


## -parameters




### -param pContext [out]

Context in which the error occurred. For a list of context values, see the 
<a href="https://msdn.microsoft.com/c9d98518-6f2e-4fd1-b0ee-6735c6d6ecd9">BG_ERROR_CONTEXT</a> enumeration.


### -param pCode






#### - pErrorCode [out]

Error code of the error that occurred.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM HRESULT values on error.




## -see-also




<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="https://msdn.microsoft.com/57323f38-c2e6-4e40-b357-7df758899f97">IBackgroundCopyError::GetErrorDescription</a>



<a href="https://msdn.microsoft.com/7b6d4bd4-2102-4e6b-b250-1d73fae94cf9">IBackgroundCopyError::GetFile</a>
 

 

