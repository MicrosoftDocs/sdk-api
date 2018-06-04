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

# AssociateFileEx function


## -description


Associates a file with an asnychronous context.


## -parameters




### -param hFile [in]

A file handle that should be in the context. It is created with the FILE_FLAG_OVERLAPPED flag set for asynchronous I/O operations. 



### -param fStoreWithDots

TBD


### -param fStoredWithTerminatingDot [in]

A flag that indicates whether the terminating dot is included in an object. If this parameter is set to <b>TRUE</b>, the object is stored with a terminating dot. 

The terminating dot is used by the NNTP/SMTP protocol to identify the end of message.


#### - fStoredWithDots [in]

If set to <b>TRUE</b>, this object was stored with dot stuffing.


## -returns



Returns a pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that was obtained. If the function fails, it returns <b>NULL</b>.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

