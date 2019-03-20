---
UID: NF:fsrmpipeline.IFsrmPipelineModuleConnector.Bind
title: IFsrmPipelineModuleConnector::Bind (fsrmpipeline.h)
author: windows-sdk-content
description: Binds the pipeline module implementation to the FSRM communication channel.
old-location: fsrm\ifsrmpipelinemoduleconnector_bind.htm
tech.root: fsrm
ms.assetid: 4ac8ecc7-a02e-46ce-ac95-35a7dd38e631
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Bind, Bind method [File Server Resource Manager], Bind method [File Server Resource Manager],FsrmPipelineModuleConnector class, Bind method [File Server Resource Manager],IFsrmPipelineModuleConnector interface, FsrmPipelineModuleConnector class [File Server Resource Manager],Bind method, IFsrmPipelineModuleConnector interface [File Server Resource Manager],Bind method, IFsrmPipelineModuleConnector.Bind, IFsrmPipelineModuleConnector::Bind, fs.ifsrmpipelinemoduleconnector_bind, fsrm.ifsrmpipelinemoduleconnector_bind, fsrmpipeline/IFsrmPipelineModuleConnector::Bind
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPipelineModuleConnector.Bind
 - FsrmPipelineModuleConnector.Bind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

