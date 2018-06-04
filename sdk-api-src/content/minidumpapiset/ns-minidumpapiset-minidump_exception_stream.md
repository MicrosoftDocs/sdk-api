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

# MINIDUMP_EXCEPTION_STREAM structure


## -description


Represents an exception information stream.


## -struct-fields




### -field ThreadId

The identifier of the thread that caused the exception.


### -field __alignment

A variable for alignment.


### -field ExceptionRecord

A 
<a href="https://msdn.microsoft.com/edbb87a7-1b99-46bd-8797-c806861ec73a">MINIDUMP_EXCEPTION</a> structure.


### -field ThreadContext

A 
<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


## -remarks



In this context, a data stream is a set of data in a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/edbb87a7-1b99-46bd-8797-c806861ec73a">MINIDUMP_EXCEPTION</a>



<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

