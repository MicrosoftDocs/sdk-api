---
UID: NN:fsrmpipeline.IFsrmStorageModuleDefinition
title: IFsrmStorageModuleDefinition (fsrmpipeline.h)
description: Defines a local storage module that is used to read and write property values.
helpviewer_keywords: ["IFsrmStorageModuleDefinition","IFsrmStorageModuleDefinition interface [File Server Resource Manager]","IFsrmStorageModuleDefinition interface [File Server Resource Manager]","described","fs.ifsrmstoragemoduledefinition","fsrm.ifsrmstoragemoduledefinition","fsrm/IFsrmStorageModuleDefinition"]
old-location: fsrm\ifsrmstoragemoduledefinition.htm
tech.root: fsrm
ms.assetid: 68ecb5e6-61b0-488f-b6bb-181f253de70e
ms.date: 12/05/2018
ms.keywords: IFsrmStorageModuleDefinition, IFsrmStorageModuleDefinition interface [File Server Resource Manager], IFsrmStorageModuleDefinition interface [File Server Resource Manager],described, fs.ifsrmstoragemoduledefinition, fsrm.ifsrmstoragemoduledefinition, fsrm/IFsrmStorageModuleDefinition
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
 - IFsrmStorageModuleDefinition
 - fsrmpipeline/IFsrmStorageModuleDefinition
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
 - IFsrmStorageModuleDefinition
---

# IFsrmStorageModuleDefinition interface


## -description

Defines a local storage module that is used to read and write property values.<div class="alert"><b>Note</b>  This interface supports local use only. Remote operations are not supported.</div>
<div> </div>


To create a storage module definition, call the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">IFsrmClassificationManager::CreateModuleDefinition</a> method.

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

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a>