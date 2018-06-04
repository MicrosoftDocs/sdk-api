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

# IMemInputPin::NotifyAllocator


## -description



The <code>NotifyAllocator</code> method specifies an allocator for the connection.




## -parameters




### -param pAllocator [in]

Pointer to the allocator's <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> interface.


### -param bReadOnly [out]

Flag that specifies whether samples from this allocator are read-only. If <b>TRUE</b>, samples are read-only.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin. The output pin might use the allocator that the input pin proposed in the <a href="https://msdn.microsoft.com/ab49028e-ae27-4d4e-a5f1-a086ade25c5e">IMemInputPin::GetAllocator</a> method, or it might provide its own allocator.

If the <i>bReadOnly</i> parameter is <b>TRUE</b>, all samples in the allocator are read-only. The filter must copy them to modify the data.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 

