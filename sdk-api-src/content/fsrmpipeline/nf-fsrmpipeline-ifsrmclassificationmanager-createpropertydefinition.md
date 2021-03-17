---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CreatePropertyDefinition
title: IFsrmClassificationManager::CreatePropertyDefinition (fsrmpipeline.h)
description: Creates a property definition.
helpviewer_keywords: ["CreatePropertyDefinition","CreatePropertyDefinition method [File Server Resource Manager]","CreatePropertyDefinition method [File Server Resource Manager]","FsrmClassificationManager class","CreatePropertyDefinition method [File Server Resource Manager]","IFsrmClassificationManager interface","CreatePropertyDefinition method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","CreatePropertyDefinition method","IFsrmClassificationManager interface [File Server Resource Manager]","CreatePropertyDefinition method","IFsrmClassificationManager.CreatePropertyDefinition","IFsrmClassificationManager2 interface [File Server Resource Manager]","CreatePropertyDefinition method","IFsrmClassificationManager2::CreatePropertyDefinition","IFsrmClassificationManager::CreatePropertyDefinition","fs.ifsrmclassificationmanager_createpropertydefinition","fsrm.ifsrmclassificationmanager_createpropertydefinition","fsrmpipeline/IFsrmClassificationManager2::CreatePropertyDefinition","fsrmpipeline/IFsrmClassificationManager::CreatePropertyDefinition"]
old-location: fsrm\ifsrmclassificationmanager_createpropertydefinition.htm
tech.root: fsrm
ms.assetid: 92c6198b-08b6-4ea6-b8de-1a21acd235d1
ms.date: 12/05/2018
ms.keywords: CreatePropertyDefinition, CreatePropertyDefinition method [File Server Resource Manager], CreatePropertyDefinition method [File Server Resource Manager],FsrmClassificationManager class, CreatePropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, CreatePropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager interface [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager.CreatePropertyDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],CreatePropertyDefinition method, IFsrmClassificationManager2::CreatePropertyDefinition, IFsrmClassificationManager::CreatePropertyDefinition, fs.ifsrmclassificationmanager_createpropertydefinition, fsrm.ifsrmclassificationmanager_createpropertydefinition, fsrmpipeline/IFsrmClassificationManager2::CreatePropertyDefinition, fsrmpipeline/IFsrmClassificationManager::CreatePropertyDefinition
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
 - IFsrmClassificationManager::CreatePropertyDefinition
 - fsrmpipeline/IFsrmClassificationManager::CreatePropertyDefinition
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
 - IFsrmClassificationManager.CreatePropertyDefinition
 - IFsrmClassificationManager2.CreatePropertyDefinition
 - FsrmClassificationManager.CreatePropertyDefinition
---

# IFsrmClassificationManager::CreatePropertyDefinition


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Creates a property definition.

## -parameters

### -param propertyDefinition [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertydefinition">IFsrmPropertyDefinition</a> interface to the 
      new property definition. To save the property definition, call 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmPropertyDefinition::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

You create a property definition to define the property that you want to use to classify files. One or more 
    classification rules can specify the property. The FSRM server limits the number of property definitions to 
    100.

You cannot delete a property that is referenced by a rule or report job.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getpropertydefinition">IFsrmClassificationManager::GetPropertyDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationrule-get_propertyaffected">IFsrmClassificationRule::PropertyAffected</a>



<b>MSFT_FSRMClassification</b>