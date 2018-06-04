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

# InsertFile function


## -description


Inserts a file into the cache.


## -parameters




### -param lpstrName [in]

The name of the file to be inserted.


### -param pContext [in]

A pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the file being inserted.


### -param fKeepReference [in]

Specifies whether the reference to the file is to be kept. If <b>TRUE</b>, the user must make a call to <a href="Http://go.microsoft.com/fwlink/p/?linkid=85303">ReleaseContext</a> for the inserted <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>.


## -returns



Returns <b>TRUE</b> if the file is inserted; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85303">ReleaseContext</a>
 

 

