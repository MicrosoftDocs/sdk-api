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

# IMemoryData::SetBuffer


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Initializes a memory buffer with a pointer to memory and length.




## -parameters




### -param cbSize [in]

Size of memory pointed to by <i>pbData</i>, in bytes.


### -param pbData [in]

Pointer to memory that this object will use.


### -param dwFlags [in]

Reserved for flag data. Must be zero.


## -returns



Returns S_OK if successful or E_INVALIDARG if <i>cbSize</i> is zero or <i>pbData</i> is <b>NULL</b>.




## -remarks



This method can be called as often as needed. When using <a href="https://msdn.microsoft.com/5f56e3f9-443b-4d67-bfed-3210e691ad4b">IStreamSample::Update</a> to update samples asynchronously, make sure that SetBuffer is never called before an update is completed.




## -see-also




<a href="https://msdn.microsoft.com/0e809ae7-381c-4ada-8940-5d42bf5c03da">IMemoryData Interface</a>
 

 

