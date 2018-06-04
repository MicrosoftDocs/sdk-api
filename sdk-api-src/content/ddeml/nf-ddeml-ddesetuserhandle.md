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

# DdeSetUserHandle function


## -description


Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the <a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a> function to retrieve this value. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation. 


### -param id [in]

Type: <b>DWORD</b>

The transaction identifier to associate with the value specified by the 
					<i>hUser</i> parameter. An application should set this parameter to QID_SYNC to associate 
					<i>hUser</i> with the conversation identified by the 
					<i>hConv</i> parameter. 


### -param hUser [in]

Type: <b>DWORD_PTR</b>

The value to be associated with the conversation handle. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

