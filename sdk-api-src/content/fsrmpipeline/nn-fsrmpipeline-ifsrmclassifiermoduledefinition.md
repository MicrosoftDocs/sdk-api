---
UID: NN:fsrmpipeline.IFsrmClassifierModuleDefinition
title: IFsrmClassifierModuleDefinition (fsrmpipeline.h)
description: Defines a classifier module.
helpviewer_keywords: ["IFsrmClassifierModuleDefinition","IFsrmClassifierModuleDefinition interface [File Server Resource Manager]","IFsrmClassifierModuleDefinition interface [File Server Resource Manager]","described","fs.ifsrmclassifiermoduledefinition","fsrm.ifsrmclassifiermoduledefinition","fsrm/IFsrmClassifierModuleDefinition"]
old-location: fsrm\ifsrmclassifiermoduledefinition.htm
tech.root: fsrm
ms.assetid: 6e691670-d7d7-48cb-8a81-ee8828b39b30
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleDefinition, IFsrmClassifierModuleDefinition interface [File Server Resource Manager], IFsrmClassifierModuleDefinition interface [File Server Resource Manager],described, fs.ifsrmclassifiermoduledefinition, fsrm.ifsrmclassifiermoduledefinition, fsrm/IFsrmClassifierModuleDefinition
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmClassifierModuleDefinition
 - fsrmpipeline/IFsrmClassifierModuleDefinition
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
 - IFsrmClassifierModuleDefinition
---

# IFsrmClassifierModuleDefinition interface


## -description

Defines a classifier module.

To create a classifier module definition, call the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a> method.

The following methods can return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">IFsrmClassificationManager::GetModuleDefinition</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduledefinition">IFsrmStorageModuleDefinition</a>