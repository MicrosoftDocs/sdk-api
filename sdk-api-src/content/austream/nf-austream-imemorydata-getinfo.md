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

# IMemoryData::GetInfo


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves information describing an audio data object.




## -parameters




### -param pdwLength [out]

Length of memory in bytes, if non-<b>NULL</b>.


### -param ppbData [out]

Pointer to the memory, if non-<b>NULL</b>.


### -param pcbActualData [out]

Length of data in bytes, if non-<b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method determines how much data the object currently contains as last set by <a href="https://msdn.microsoft.com/22d9c24b-deb0-429a-ad9c-f6d286c7cdeb">SetActual</a>.




## -see-also




<a href="https://msdn.microsoft.com/0e809ae7-381c-4ada-8940-5d42bf5c03da">IMemoryData Interface</a>
 

 

