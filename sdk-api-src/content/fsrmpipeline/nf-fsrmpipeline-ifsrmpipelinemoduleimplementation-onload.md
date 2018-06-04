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

# IFsrmPipelineModuleImplementation::OnLoad


## -description


Initializes the pipeline module.


## -parameters




### -param moduleDefinition [in]

Type: <b><a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a>*</b>

An <a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a> 
       instance representing the pipeline module definition to use.


### -param moduleConnector [out]

Type: <b><a href="https://msdn.microsoft.com/7debbe8c-b687-42e1-b9b7-1b5f6f16a159">IFsrmPipelineModuleConnector</a>**</b>

An <a href="https://msdn.microsoft.com/7debbe8c-b687-42e1-b9b7-1b5f6f16a159">IFsrmPipelineModuleConnector</a> instance 
       representing the pipeline module connector to use.


## -returns



Type: <b>HRESULT</b>

The method returns the following return values.

Other values will result in the client application receiving a 
         <b>FSRM_E_UNEXPECTED</b><b>FSRM_E_MODULE_SESSION_INITIALIZATION</b> 
         error.

<b>Windows Server 2008 R2:  </b>The client application will receive a <b>FSRM_E_UNEXPECTED</b> error.




## -remarks



Your <b>OnLoad</b> implementation 
    must create and bind to an instance of an object implementing the 
    <a href="https://msdn.microsoft.com/7debbe8c-b687-42e1-b9b7-1b5f6f16a159">IFsrmPipelineModuleConnector</a> interface and 
    return it in the <i>moduleConnector</i> parameter. For more information on how to create and 
    bind this instance, see 
    <a href="https://msdn.microsoft.com/92568969-7ee6-4584-a400-ee2aa79961e8">Initializing and Binding a Pipeline Module</a>.


#### Examples

See 
     <a href="https://msdn.microsoft.com/25175db9-9ed5-4189-b9fd-5c4102f1d287">Developing FCI Pipeline Modules</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a>



<a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a>



<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 

