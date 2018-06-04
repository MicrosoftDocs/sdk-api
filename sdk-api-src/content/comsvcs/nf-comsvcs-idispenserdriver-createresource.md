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

# IDispenserDriver::CreateResource


## -description


Creates a resource.


## -parameters




### -param ResTypId [in]

The type of resource to be created.


### -param pResId [out]

A handle to the newly created resource.


### -param pSecsFreeBeforeDestroy [out]

The time-out of the new resource. This is the number of seconds that this resource is allowed to remain idle in the pool before it is destroyed.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



The <b>CreateResource</b> method is called by the Dispenser Manager in the following cases:

<ul>
<li>When a resource is needed and there is no inventory to satisfy an <a href="https://msdn.microsoft.com/2b6c5d54-4917-460f-9740-abe4b578761f">IHolder::AllocResource</a> call when none were found in inventory.</li>
<li>When the Dispenser Manager is setting up initial inventory.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>
 

 

