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

# IWMWriterSink::AllocateDataUnit


## -description



The <b>AllocateDataUnit</b> method is called by the writer object when it needs a buffer to deliver a data unit. Your implementation of this method returns a buffer of at least the size passed in. You can manage buffers internally in any way that you like. The simplest method is to create a new buffer object for each call, but doing so is quite inefficient. Instead, most sinks maintain several buffers that are reused.




## -parameters




### -param cbDataUnit [in]

Size of the data unit that the writer needs to deliver, in bytes. The buffer you assign to <i>ppDataUnit</i> must be this size or bigger.


### -param ppDataUnit [out]

On return, set to a pointer to the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface of a buffer object.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>
 

 

