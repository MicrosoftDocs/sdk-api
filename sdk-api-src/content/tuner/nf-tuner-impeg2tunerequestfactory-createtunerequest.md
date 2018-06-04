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

# IMPEG2TuneRequestFactory::CreateTuneRequest


## -description


The <b>CreateTuneRequest</b> method creates the minimal MPEG-2 tune request for a specified tuning space.


## -parameters




### -param TuningSpace [in]

Pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the tuning space.


### -param TuneRequest [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/a9e37b8b-9272-43c6-b36e-1e82b0d1b0db">IMPEG2TuneRequest</a> interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/0fbeab7d-0c54-45e3-a73c-755df28a16d5">IMPEG2TuneRequestFactory Interface</a>
 

 

