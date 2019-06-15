---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetModuleDefinition
title: IFsrmClassificationManager::GetModuleDefinition (fsrmpipeline.h)
author: windows-sdk-content
description: Retrieves the specified module definition.
old-location: fsrm\ifsrmclassificationmanager_getmoduledefinition.htm
tech.root: fsrm
ms.assetid: 41272218-25af-4c8f-8730-37a08a7fad4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetModuleDefinition method, GetModuleDefinition, GetModuleDefinition method [File Server Resource Manager], GetModuleDefinition method [File Server Resource Manager],FsrmClassificationManager class, GetModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, GetModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetModuleDefinition method, IFsrmClassificationManager.GetModuleDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],GetModuleDefinition method, IFsrmClassificationManager2::GetModuleDefinition, IFsrmClassificationManager::GetModuleDefinition, fs.ifsrmclassificationmanager_getmoduledefinition, fsrm.ifsrmclassificationmanager_getmoduledefinition, fsrmpipeline/IFsrmClassificationManager2::GetModuleDefinition, fsrmpipeline/IFsrmClassificationManager::GetModuleDefinition
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
ms.custom: 19H1
---

# IFsrmClassificationManager::GetModuleDefinition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Retrieves the specified module definition.


## -parameters




### -param moduleName [in]

The name of the module to retrieve. Must not exceed 100 characters in length.


### -param moduleType [in]

The type of the module to retrieve. For possible types, see the 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmenums/ne-fsrmenums-_fsrmpipelinemoduletype">FsrmPipelineModuleType</a> enumeration.


### -param moduleDefinition [out]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a> 
      interface to  the retrieved module definition. Query the 
      <b>IFsrmPipelineModuleDefinition</b> interface to 
      get the interface for the specified module. For example, if <i>moduleType</i> is 
      <b>FsrmPipelineModuleType_Classifier</b>, query the 
      <b>IFsrmPipelineModuleDefinition</b> interface for 
      the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a> 
      interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduledefinition">IFsrmStorageModuleDefinition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
 

 

