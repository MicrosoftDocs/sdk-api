---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.UseRulesAndDefinitions
title: IFsrmClassifierModuleImplementation::UseRulesAndDefinitions (fsrmpipeline.h)
description: Specifies the collection of rules and relevant property definitions the classifier should expect to process.
helpviewer_keywords: ["IFsrmClassifierModuleImplementation interface [File Server Resource Manager]","UseRulesAndDefinitions method","IFsrmClassifierModuleImplementation.UseRulesAndDefinitions","IFsrmClassifierModuleImplementation::UseRulesAndDefinitions","UseRulesAndDefinitions","UseRulesAndDefinitions method [File Server Resource Manager]","UseRulesAndDefinitions method [File Server Resource Manager]","IFsrmClassifierModuleImplementation interface","fs.ifsrmclassifiermoduleimplementation_userulesanddefinitions","fsrm.ifsrmclassifiermoduleimplementation_userulesanddefinitions","fsrmpipeline/IFsrmClassifierModuleImplementation::UseRulesAndDefinitions"]
old-location: fsrm\ifsrmclassifiermoduleimplementation_userulesanddefinitions.htm
tech.root: fsrm
ms.assetid: 8fbca8c4-7021-4183-b8f7-a32082da17fc
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleImplementation interface [File Server Resource Manager],UseRulesAndDefinitions method, IFsrmClassifierModuleImplementation.UseRulesAndDefinitions, IFsrmClassifierModuleImplementation::UseRulesAndDefinitions, UseRulesAndDefinitions, UseRulesAndDefinitions method [File Server Resource Manager], UseRulesAndDefinitions method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, fs.ifsrmclassifiermoduleimplementation_userulesanddefinitions, fsrm.ifsrmclassifiermoduleimplementation_userulesanddefinitions, fsrmpipeline/IFsrmClassifierModuleImplementation::UseRulesAndDefinitions
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
 - IFsrmClassifierModuleImplementation::UseRulesAndDefinitions
 - fsrmpipeline/IFsrmClassifierModuleImplementation::UseRulesAndDefinitions
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
 - IFsrmClassifierModuleImplementation.UseRulesAndDefinitions
---

# IFsrmClassifierModuleImplementation::UseRulesAndDefinitions


## -description

Specifies the collection of rules and relevant property definitions the classifier should expect to 
    process.

## -parameters

### -param rules [in]

Type: <b><a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>*</b>

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> instance representing a collection 
       of rules that will be used during the current classification session.

### -param propertyDefinitions [in]

Type: <b><a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>*</b>

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> instance representing a collection 
       of property definitions that are referenced by the specified collection of rules.

## -returns

Type: <b>HRESULT</b>

The method returns the following return values.

Other values will result in the client application receiving a 
         <b>FSRM_E_MODULE_SESSION_INITIALIZATION</b> error.

<b>Windows Server 2008 R2:  </b>The client application will receive a <b>FSRM_E_UNEXPECTED</b> error.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>