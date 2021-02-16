---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumModuleDefinitions
title: IFsrmClassificationManager::EnumModuleDefinitions (fsrmpipeline.h)
description: Enumerates the module definitions of the specified type.
helpviewer_keywords: ["EnumModuleDefinitions","EnumModuleDefinitions method [File Server Resource Manager]","EnumModuleDefinitions method [File Server Resource Manager]","FsrmClassificationManager class","EnumModuleDefinitions method [File Server Resource Manager]","IFsrmClassificationManager interface","EnumModuleDefinitions method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","EnumModuleDefinitions method","IFsrmClassificationManager interface [File Server Resource Manager]","EnumModuleDefinitions method","IFsrmClassificationManager.EnumModuleDefinitions","IFsrmClassificationManager2 interface [File Server Resource Manager]","EnumModuleDefinitions method","IFsrmClassificationManager2::EnumModuleDefinitions","IFsrmClassificationManager::EnumModuleDefinitions","fs.ifsrmclassificationmanager_enummoduledefinitions","fsrm.ifsrmclassificationmanager_enummoduledefinitions","fsrmpipeline/IFsrmClassificationManager2::EnumModuleDefinitions","fsrmpipeline/IFsrmClassificationManager::EnumModuleDefinitions"]
old-location: fsrm\ifsrmclassificationmanager_enummoduledefinitions.htm
tech.root: fsrm
ms.assetid: eeda0802-e450-4a8b-a08c-135784540b17
ms.date: 12/05/2018
ms.keywords: EnumModuleDefinitions, EnumModuleDefinitions method [File Server Resource Manager], EnumModuleDefinitions method [File Server Resource Manager],FsrmClassificationManager class, EnumModuleDefinitions method [File Server Resource Manager],IFsrmClassificationManager interface, EnumModuleDefinitions method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager interface [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager.EnumModuleDefinitions, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumModuleDefinitions method, IFsrmClassificationManager2::EnumModuleDefinitions, IFsrmClassificationManager::EnumModuleDefinitions, fs.ifsrmclassificationmanager_enummoduledefinitions, fsrm.ifsrmclassificationmanager_enummoduledefinitions, fsrmpipeline/IFsrmClassificationManager2::EnumModuleDefinitions, fsrmpipeline/IFsrmClassificationManager::EnumModuleDefinitions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmClassificationManager::EnumModuleDefinitions
 - fsrmpipeline/IFsrmClassificationManager::EnumModuleDefinitions
dev_langs:
 - c++
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
---

# IFsrmClassificationManager::EnumModuleDefinitions


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Enumerates the module definitions of the specified type.

## -parameters

### -param moduleType [in]

Type of module to enumerate. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpipelinemoduletype">FsrmPipelineModuleType</a> enumeration.

### -param options [in]

One or more options for enumerating the modules. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported by this method.</div>
<div> </div>

### -param moduleDefinitions [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
       collection of module definitions. Each item in the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a> 
       interface. You can then use the 
       <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_moduletype">IFsrmPipelineModuleDefinition.ModuleType</a> 
       property to determine the module's type. Query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the module interface to use. For example, if 
       <b>ModuleType</b> is 
       <b>FsrmPipelineModuleType_Classifier</b>, query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a> 
       interface.

The collection contains only committed module definitions; the collection will not contain newly created 
       module definitions that have not been committed.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduledefinition">IFsrmStorageModuleDefinition</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>