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

# _WER_EXCEPTION_INFORMATION structure


## -description


Contains exception information for the <a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a> function.


## -struct-fields




### -field pExceptionPointers

A pointer to an <a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure.


### -field bClientPointers

A process (calling process) can provide error reporting functionality for another process (client process). If this member is <b>TRUE</b>, the exception pointer is located inside the  address space of the client process. If this member is <b>FALSE</b>, the exception pointer is located inside the address space of the calling process.


## -see-also




<a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a>
 

 

