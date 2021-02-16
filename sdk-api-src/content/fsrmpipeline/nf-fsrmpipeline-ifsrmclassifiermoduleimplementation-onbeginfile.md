---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.OnBeginFile
title: IFsrmClassifierModuleImplementation::OnBeginFile (fsrmpipeline.h)
description: Instructs the classifier to prepare for processing a file with the specified property bag.
helpviewer_keywords: ["IFsrmClassifierModuleImplementation interface [File Server Resource Manager]","OnBeginFile method","IFsrmClassifierModuleImplementation.OnBeginFile","IFsrmClassifierModuleImplementation::OnBeginFile","OnBeginFile","OnBeginFile method [File Server Resource Manager]","OnBeginFile method [File Server Resource Manager]","IFsrmClassifierModuleImplementation interface","fs.ifsrmclassifiermoduleimplementation_onbeginfile","fsrm.ifsrmclassifiermoduleimplementation_onbeginfile","fsrmpipeline/IFsrmClassifierModuleImplementation::OnBeginFile"]
old-location: fsrm\ifsrmclassifiermoduleimplementation_onbeginfile.htm
tech.root: fsrm
ms.assetid: 799f26c7-925e-4669-9571-128e10c51e9c
ms.date: 12/05/2018
ms.keywords: IFsrmClassifierModuleImplementation interface [File Server Resource Manager],OnBeginFile method, IFsrmClassifierModuleImplementation.OnBeginFile, IFsrmClassifierModuleImplementation::OnBeginFile, OnBeginFile, OnBeginFile method [File Server Resource Manager], OnBeginFile method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, fs.ifsrmclassifiermoduleimplementation_onbeginfile, fsrm.ifsrmclassifiermoduleimplementation_onbeginfile, fsrmpipeline/IFsrmClassifierModuleImplementation::OnBeginFile
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
 - IFsrmClassifierModuleImplementation::OnBeginFile
 - fsrmpipeline/IFsrmClassifierModuleImplementation::OnBeginFile
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
 - IFsrmClassifierModuleImplementation.OnBeginFile
---

# IFsrmClassifierModuleImplementation::OnBeginFile


## -description

Instructs the classifier to prepare for processing a file with the specified property bag.

## -parameters

### -param propertyBag [in]

The property bag that corresponds to the file to be processed.

### -param arrayRuleIds [in]

A <b>SAFEARRAY</b> of variants that contains one or more strings listing the identifiers of rules that will be processed. Each identifier corresponds to a rule object that is in the rule collection passed in by a previous call to the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-userulesanddefinitions">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a> method. The rule object can also be obtained by using this identifier in a call to the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-getbyid">IFsrmCollection::GetById</a> method on this collection.

## -returns

The method returns the following return values. Implementers should return an <b>HRESULT</b> error code for any other errors.

## -remarks

The classifier is not allowed to directly call <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-setfileproperty">IFsrmPropertyBag::SetFileProperty</a> on the property bag that is passed in. The classifier instead provides property values when the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a> method or the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a> method is called by FSRM.

Each of the calls to the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a> method or the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a> method is associated with a rule, the identifiers of which are passed in through the <i>arrayRuleIds</i> parameter. As an optimization, the classifier may optionally pre-compute the responses for the <b>IFsrmClassifierModuleImplementation::DoesPropertyValueApply</b> method or the <b>IFsrmClassifierModuleImplementation::GetPropertyValueToApply</b> method during the <b>OnBeginFile</b> method call using the rule identifiers passed in through the <i>arrayRuleIds</i> parameter.

If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>