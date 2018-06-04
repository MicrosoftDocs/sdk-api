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

# _WIN32_FIND_STREAM_DATA structure


## -description


Contains information about the stream found by the 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> or 
    <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a> function.


## -struct-fields




### -field StreamSize

A <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> value that specifies the 
      size of the stream, in bytes.


### -field cStreamName

The name of the stream. The string name format is 
      ":<i>streamname</i>:$<i>streamtype</i>".


## -see-also




<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

