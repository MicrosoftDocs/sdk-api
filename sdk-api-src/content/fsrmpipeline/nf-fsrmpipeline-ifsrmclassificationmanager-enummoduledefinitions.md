---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumModuleDefinitions
title: IFsrmClassificationManager::EnumModuleDefinitions
author: windows-sdk-content
description: Enumerates the module definitions of the specified type.
old-location: fsrm\ifsrmclassificationmanager_enummoduledefinitions.htm
old-project: fsrm
ms.assetid: eeda0802-e450-4a8b-a08c-135784540b17
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: EnumModuleDefinitions, EnumModuleDefinitions method [File Server Resource Manager], EnumModuleDefinitions method [File Server Resource Manager],FsrmClassificationManager class, EnumModuleDefinitions method [File Server Resource Manager],IFsrmClassificationManager interface, EnumModuleDefinitions method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager interface [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager.EnumModuleDefinitions, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager2::EnumModuleDefinitions, IFsrmClassificationManager::EnumModuleDefinitions, fs.ifsrmclassificationmanager_enummoduledefinitions, fsrm.ifsrmclassificationmanager_enummoduledefinitions, fsrmpipeline/IFsrmClassificationManager2::EnumModuleDefinitions, fsrmpipeline/IFsrmClassificationManager::EnumModuleDefinitions
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmClassificationManager.EnumModuleDefinitions
 - IFsrmClassificationManager2.EnumModuleDefinitions
 - FsrmClassificationManager.EnumModuleDefinitions
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmClassificationManager::EnumModuleDefinitions


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Enumerates the module definitions of the specified type.


## -parameters




### -param moduleType [in]

Type of module to enumerate. For possible values, see the 
      <a href="https://msdn.microsoft.com/a482c371-a01c-486b-b25b-d22283dba652">FsrmPipelineModuleType</a> enumeration.


### -param options [in]

One or more options for enumerating the modules. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported by this method.</div>
<div> </div>

### -param moduleDefinitions [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a 
       collection of module definitions. Each item in the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="https://msdn.microsoft.com/982c82a4-466d-476e-ad17-8f6f1c309c79">IFsrmPipelineModuleDefinition</a> 
       interface. You can then use the 
       <a href="https://msdn.microsoft.com/8cf3069d-8ad1-455b-baea-29c30cef1672">IFsrmPipelineModuleDefinition.ModuleType</a> 
       property to determine the module's type. Query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the module interface to use. For example, if 
       <b>ModuleType</b> is 
       <b>FsrmPipelineModuleType_Classifier</b>, query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the <a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a> 
       interface.

The collection contains only committed module definitions; the collection will not contain newly created 
       module definitions that have not been committed.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="https://msdn.microsoft.com/6e691670-d7d7-48cb-8a81-ee8828b39b30">IFsrmClassifierModuleDefinition</a>



<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

