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

# IQualityControl::Notify


## -description



The <code>Notify</code> method notifies the filter that a quality change is requested.




## -parameters




### -param pSelf [in]

Pointer to the filter that is sending the quality notification.


### -param q [in]


<a href="https://msdn.microsoft.com/2ab7fcde-0e44-4d60-acf5-3638efbe15f7">Quality</a> structure.


## -returns



Returns S_OK if the method succeeds; otherwise, returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2672e563-75d7-4a8a-b914-7b0712e856e8">IQualityControl Interface</a>
 

 

