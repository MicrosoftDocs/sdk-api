---
UID: NF:fsrmpipeline.IFsrmPipelineModuleConnector.Bind
title: IFsrmPipelineModuleConnector::Bind (fsrmpipeline.h)
description: Binds the pipeline module implementation to the FSRM communication channel.
helpviewer_keywords: ["Bind","Bind method [File Server Resource Manager]","Bind method [File Server Resource Manager]","FsrmPipelineModuleConnector class","Bind method [File Server Resource Manager]","IFsrmPipelineModuleConnector interface","FsrmPipelineModuleConnector class [File Server Resource Manager]","Bind method","IFsrmPipelineModuleConnector interface [File Server Resource Manager]","Bind method","IFsrmPipelineModuleConnector.Bind","IFsrmPipelineModuleConnector::Bind","fs.ifsrmpipelinemoduleconnector_bind","fsrm.ifsrmpipelinemoduleconnector_bind","fsrmpipeline/IFsrmPipelineModuleConnector::Bind"]
old-location: fsrm\ifsrmpipelinemoduleconnector_bind.htm
tech.root: fsrm
ms.assetid: 4ac8ecc7-a02e-46ce-ac95-35a7dd38e631
ms.date: 12/05/2018
ms.keywords: Bind, Bind method [File Server Resource Manager], Bind method [File Server Resource Manager],FsrmPipelineModuleConnector class, Bind method [File Server Resource Manager],IFsrmPipelineModuleConnector interface, FsrmPipelineModuleConnector class [File Server Resource Manager],Bind method, IFsrmPipelineModuleConnector interface [File Server Resource Manager],Bind method, IFsrmPipelineModuleConnector.Bind, IFsrmPipelineModuleConnector::Bind, fs.ifsrmpipelinemoduleconnector_bind, fsrm.ifsrmpipelinemoduleconnector_bind, fsrmpipeline/IFsrmPipelineModuleConnector::Bind
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
 - IFsrmPipelineModuleConnector::Bind
 - fsrmpipeline/IFsrmPipelineModuleConnector::Bind
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
 - IFsrmPipelineModuleConnector.Bind
 - FsrmPipelineModuleConnector.Bind
---

## -description

Binds the pipeline module implementation to the FSRM communication channel.

## -parameters

### -param moduleDefinition [in]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a> interface that contains the definition of the module.

### -param moduleImplementation [in]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a> interface to the module's implementation.

## -returns

The method returns the following return values.

## -remarks

Call this method from your <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onload">IFsrmPipelineModuleImplementation::OnLoad</a> implementation.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmpipelinemoduleconnector">FsrmPipelineModuleConnector</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleconnector">IFsrmPipelineModuleConnector</a>
