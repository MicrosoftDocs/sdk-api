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

# IWsbApplicationAsync::QueryStatus


## -description


Queries the status of an asynchronous operation.


## -parameters




### -param phrResult [out]

The address of an <b>HRESULT</b> value that receives the status of the current asynchronous operation. If the asynchronous operation fails, this parameter receives the failure status code. Possible values include the following.



#### S_OK (0)

The asynchronous operation was completed successfully.



#### WSBAPP_ASYNC_IN_PROGRESS (0x407A0004L)

The asynchronous operation is still running.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Windows Server Backup calls this  method periodically to query the status of a pending asynchronous operation.




## -see-also




<a href="https://msdn.microsoft.com/cd8f74c0-c2dc-487c-b702-1e1355e99b7d">IWsbApplicationAsync</a>
 

 

