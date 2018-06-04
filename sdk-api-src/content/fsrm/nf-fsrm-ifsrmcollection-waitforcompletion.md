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

# IFsrmCollection::WaitForCompletion


## -description


Limits the time that an asynchronous collection can take to collect the objects.<div class="alert"><b>Note</b>  Asynchronous collections are not supported by FSRM, therefore this method always sets the <i>completed</i> parameter to <b>VARIANT_TRUE</b>.</div>
<div> </div>



## -parameters




### -param waitSeconds [in]

The number of seconds to wait for the collection to finish collecting objects. To wait indefinitely, set this parameter to –1.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the collection finished collecting objects in the time specified; otherwise, <b>VARIANT_FALSE</b>.


## -returns



This method is not supported and always returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

