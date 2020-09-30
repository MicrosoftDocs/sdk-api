---
UID: NF:fsrmpipeline.IFsrmPipelineModuleImplementation.OnLoad
title: IFsrmPipelineModuleImplementation::OnLoad (fsrmpipeline.h)
description: Initializes the pipeline module.
helpviewer_keywords: ["IFsrmClassifierModuleImplementation interface [File Server Resource Manager]","OnLoad method","IFsrmClassifierModuleImplementation::OnLoad","IFsrmPipelineModuleImplementation interface [File Server Resource Manager]","OnLoad method","IFsrmPipelineModuleImplementation.OnLoad","IFsrmPipelineModuleImplementation::OnLoad","IFsrmStorageModuleImplementation interface [File Server Resource Manager]","OnLoad method","IFsrmStorageModuleImplementation::OnLoad","OnLoad","OnLoad method [File Server Resource Manager]","OnLoad method [File Server Resource Manager]","IFsrmClassifierModuleImplementation interface","OnLoad method [File Server Resource Manager]","IFsrmPipelineModuleImplementation interface","OnLoad method [File Server Resource Manager]","IFsrmStorageModuleImplementation interface","fs.ifsrmpipelinemoduleimplementation_onload","fsrm.ifsrmpipelinemoduleimplementation_onload","fsrmpipeline/IFsrmClassifierModuleImplementation::OnLoad","fsrmpipeline/IFsrmPipelineModuleImplementation::OnLoad","fsrmpipeline/IFsrmStorageModuleImplementation::OnLoad"]
old-location: fsrm\ifsrmpipelinemoduleimplementation_onload.htm
tech.root: fsrm
ms.assetid: 69d848b9-4143-4b6c-9a45-66ff44c54b66
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleImplementation interface [File Server Resource Manager],OnLoad method, IFsrmClassifierModuleImplementation::OnLoad, IFsrmPipelineModuleImplementation interface [File Server Resource Manager],OnLoad method, IFsrmPipelineModuleImplementation.OnLoad, IFsrmPipelineModuleImplementation::OnLoad, IFsrmStorageModuleImplementation interface [File Server Resource Manager],OnLoad method, IFsrmStorageModuleImplementation::OnLoad, OnLoad, OnLoad method [File Server Resource Manager], OnLoad method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, OnLoad method [File Server Resource Manager],IFsrmPipelineModuleImplementation interface, OnLoad method [File Server Resource Manager],IFsrmStorageModuleImplementation interface, fs.ifsrmpipelinemoduleimplementation_onload, fsrm.ifsrmpipelinemoduleimplementation_onload, fsrmpipeline/IFsrmClassifierModuleImplementation::OnLoad, fsrmpipeline/IFsrmPipelineModuleImplementation::OnLoad, fsrmpipeline/IFsrmStorageModuleImplementation::OnLoad
req.header: fsrmpipeline.h
req.include-header: 
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
 - IFsrmPipelineModuleImplementation::OnLoad
 - fsrmpipeline/IFsrmPipelineModuleImplementation::OnLoad
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
 - IFsrmPipelineModuleImplementation.OnLoad
 - IFsrmStorageModuleImplementation.OnLoad
 - IFsrmClassifierModuleImplementation.OnLoad
---

# IFsrmPipelineModuleImplementation::OnLoad


## -description

Initializes the pipeline module.

## -parameters

### -param moduleDefinition [in]

Type: <b><a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>*</b>

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a> 
       instance representing the pipeline module definition to use.

### -param moduleConnector [out]

Type: <b><a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleconnector">IFsrmPipelineModuleConnector</a>**</b>

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleconnector">IFsrmPipelineModuleConnector</a> instance 
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
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleconnector">IFsrmPipelineModuleConnector</a> interface and 
    return it in the <i>moduleConnector</i> parameter. For more information on how to create and 
    bind this instance, see 
    <a href="/previous-versions/windows/desktop/fsrm/initializing-and-binding-a-pipeline-module">Initializing and Binding a Pipeline Module</a>.


#### Examples

See 
     <a href="/previous-versions/windows/desktop/fsrm/developing-fci-pipeline-modules">Developing FCI Pipeline Modules</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>