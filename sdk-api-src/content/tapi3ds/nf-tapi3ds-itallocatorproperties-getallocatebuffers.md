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

# ITAllocatorProperties::GetAllocateBuffers


## -description


The 
<b>GetAllocateBuffers</b> method determines whether the current allocator buffers can be retrieved. If it returns <b>FALSE</b>, the sample that the MST allocated doesn't have any buffers and they must be supplied before <b>Update</b> is called on the samples.


## -parameters




### -param pbAllocBuffers [out]

Indicates whether allocator buffers have been set.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/a0facf08-1b03-415b-b97e-3fda5a164b89">ITAllocatorProperties</a>
 

 

