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

# EngQueryFileTimeStamp function


## -description


The <b>EngQueryFileTimeStamp</b> function returns the time stamp of a file.


## -parameters




### -param pwsz [in]

Pointer to a null-terminated string containing the name of the file to be queried.


## -returns



<b>EngQueryFileTimeStamp</b> returns the last time the file was written to upon success. It returns <b>NULL</b> if it fails.




## -remarks



The time returned is local system time for the current time zone, specified in system-time format. Absolute system time is the number of 100-nanosecond intervals since the start of 1601.



