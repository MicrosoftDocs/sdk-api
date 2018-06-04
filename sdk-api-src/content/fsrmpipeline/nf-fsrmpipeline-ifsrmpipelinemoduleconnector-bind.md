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

# IFsrmPipelineModuleConnector::Bind


## -description


Binds the pipeline module implementation to the FSRM communication channel.


## -parameters




### -param moduleDefinition [in]

An <a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a> interface that contains the definition of the module.


### -param moduleImplementation [in]

An <a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a> interface to the module's implementation.


#### - rules [in]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a collection of rules.


## -returns



The method returns the following return values.




## -remarks



Call this method from your <a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">IFsrmPipelineModuleImplementation::OnLoad</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/b00f4d1f-2920-4ec4-ae90-756b2600198b">FsrmPipelineModuleConnector</a>



<a href="https://msdn.microsoft.com/7debbe8c-b687-42e1-b9b7-1b5f6f16a159">IFsrmPipelineModuleConnector</a>
 

 

