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

# IMFSourceReaderCallback2::OnStreamError


## -description


Called when an asynchronous error occurs with the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>.


## -parameters




### -param dwStreamIndex

The index of the stream of the transform that raised the asynchronous error.


### -param hrStatus

The error that occurred.


## -returns



Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.




## -see-also




<a href="https://msdn.microsoft.com/D0EC7FE9-74C3-4A7C-A5F3-798A3D6EF2CC">IMFSourceReaderCallback2</a>
 

 

