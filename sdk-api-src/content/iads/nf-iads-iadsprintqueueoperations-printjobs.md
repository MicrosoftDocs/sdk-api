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

# IADsPrintQueueOperations::PrintJobs


## -description


The <b>IADsPrintQueueOperations::PrintJobs</b> method gets an  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface pointer on the collection of the print jobs processed in this print queue. This collection can be enumerated using the standard Automation enumeration methods on  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>. To delete a print job, use the  <a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a> method on the retrieved interface pointer.


## -parameters




### -param pObject






#### - ppPrintJobs [out]

Pointer to a pointer to the  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface on the collection of objects added to this print queue. Objects in the collection implement the  <a href="https://msdn.microsoft.com/82d61e39-4dbb-41c9-85d5-6f4e7ab7f66b">IADsPrintJob</a> interface.


## -returns



This method supports the standard return values. For more information about other return values, see the  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a>



<a href="https://msdn.microsoft.com/82d61e39-4dbb-41c9-85d5-6f4e7ab7f66b">IADsPrintJob</a>



<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">IADsPrintJob Property Methods</a>



<a href="https://msdn.microsoft.com/97495455-a576-4984-beb8-9282073e88c2">IADsPrintQueueOperations</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

