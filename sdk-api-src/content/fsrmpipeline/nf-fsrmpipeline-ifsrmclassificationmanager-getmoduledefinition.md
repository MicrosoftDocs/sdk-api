---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetModuleDefinition
title: IFsrmClassificationManager::GetModuleDefinition
author: windows-sdk-content
description: Retrieves the specified module definition.
old-location: fsrm\ifsrmclassificationmanager_getmoduledefinition.htm
tech.root: fsrm
ms.assetid: 41272218-25af-4c8f-8730-37a08a7fad4f
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetModuleDefinition method, GetModuleDefinition, GetModuleDefinition method [File Server Resource Manager], GetModuleDefinition method [File Server Resource Manager],FsrmClassificationManager class, GetModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, GetModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetModuleDefinition method, IFsrmClassificationManager.GetModuleDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],GetModuleDefinition method, IFsrmClassificationManager2::GetModuleDefinition, IFsrmClassificationManager::GetModuleDefinition, fs.ifsrmclassificationmanager_getmoduledefinition, fsrm.ifsrmclassificationmanager_getmoduledefinition, fsrmpipeline/IFsrmClassificationManager2::GetModuleDefinition, fsrmpipeline/IFsrmClassificationManager::GetModuleDefinition
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmClassificationManager.GetModuleDefinition
 - IFsrmClassificationManager2.GetModuleDefinition
 - FsrmClassificationManager.GetModuleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationManager::GetModuleDefinition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Retrieves the specified module definition.


## -parameters




### -param moduleName [in]

The name of the module to retrieve. Must not exceed 100 characters in length.


### -param moduleType [in]

The type of the module to retrieve. For possible types, see the 
      <a href="https://msdn.microsoft.com/a482c371-a01c-486b-b25b-d22283dba652">FsrmPipelineModuleType</a> enumeration.


### -param moduleDefinition [out]

An <a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a> 
      interface to  the retrieved module definition. Query the 
      <b>IFsrmPipelineModuleDefinition</b> interface to 
      get the interface for the specified module. For example, if <i>moduleType</i> is 
      <b>FsrmPipelineModuleType_Classifier</b>, query the 
      <b>IFsrmPipelineModuleDefinition</b> interface for 
      the <a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a> 
      interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinition</a>



<a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a>



<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

