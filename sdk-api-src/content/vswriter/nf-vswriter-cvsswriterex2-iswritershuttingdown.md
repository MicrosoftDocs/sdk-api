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

# CVssWriterEx2::IsWriterShuttingDown


## -description


Determines whether the writer is shutting down.


## -parameters






## -returns



Returns <b>true</b> if the writer is shutting down, or <b>false</b> otherwise.




## -remarks



The writer implementation should call this method periodically during long-running events where the writer is performing a large amount of processing or looping. If this method returns <b>true</b> during the event, the writer should do the following:

<ol>
<li>Log an error to the Application Event Log event. This is optional, but recommended.</li>
<li>Call <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">SetWriterFailure</a> or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">SetWriterFailureEx</a>, passing a non-retryable error code for the <i>hr</i> or <i>hrWriter</i> parameter.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/13cdeae3-dece-42ae-8bff-037ee3e4cec4">CVssWriterEx2</a>
 

 

