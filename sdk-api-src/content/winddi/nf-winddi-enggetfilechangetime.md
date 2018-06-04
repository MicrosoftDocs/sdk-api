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

# EngGetFileChangeTime function


## -description


The <b>EngGetFileChangeTime</b> function retrieves a file's last write time.


## -parameters




### -param h [in]

Handle to the file whose change time is to be queried.


### -param pChangeTime [out]

Pointer to a LARGE_INTEGER in which the change time is returned.


## -returns



<b>EngGetFileChangeTime</b> returns <b>TRUE</b> if it succeeds in returning the timestamp; otherwise it returns <b>FALSE</b>.




## -remarks



The time returned is specified in system-time format. Absolute system time is the number of 100-nanosecond intervals since the start of the year 1601.



