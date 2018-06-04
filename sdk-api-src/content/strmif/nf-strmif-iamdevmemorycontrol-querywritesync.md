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

# IAMDevMemoryControl::QueryWriteSync


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Checks if the memory supported by the allocator requires the use of the <a href="https://msdn.microsoft.com/46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf">IAMDevMemoryControl::WriteSync</a> method.




## -parameters






## -returns



Returns S_OK if the method is required, or S_FALSE otherwise.




## -remarks



Not all on-board memory needs to have <a href="https://msdn.microsoft.com/46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf">WriteSync</a> called to synchronize with the completed write. This method is used to check if the call is necessary.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl Interface</a>
 

 

