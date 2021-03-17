---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.DoesPropertyValueApply
title: IFsrmClassifierModuleImplementation::DoesPropertyValueApply (fsrmpipeline.h)
description: Queries the classifier to find out whether the specified property value applies to the file most recently specified by the IFsrmClassifierModuleImplementation::OnBeginFile method.
helpviewer_keywords: ["DoesPropertyValueApply","DoesPropertyValueApply method [File Server Resource Manager]","DoesPropertyValueApply method [File Server Resource Manager]","IFsrmClassifierModuleImplementation interface","IFsrmClassifierModuleImplementation interface [File Server Resource Manager]","DoesPropertyValueApply method","IFsrmClassifierModuleImplementation.DoesPropertyValueApply","IFsrmClassifierModuleImplementation::DoesPropertyValueApply","fs.ifsrmclassifiermoduleimplementation_doespropertyvalueapply","fsrm.ifsrmclassifiermoduleimplementation_doespropertyvalueapply","fsrmpipeline/IFsrmClassifierModuleImplementation::DoesPropertyValueApply"]
old-location: fsrm\ifsrmclassifiermoduleimplementation_doespropertyvalueapply.htm
tech.root: fsrm
ms.assetid: ab42430c-1e30-4576-b6f8-c0488b6230dd
ms.date: 12/05/2018
ms.keywords: DoesPropertyValueApply, DoesPropertyValueApply method [File Server Resource Manager], DoesPropertyValueApply method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, IFsrmClassifierModuleImplementation interface [File Server Resource Manager],DoesPropertyValueApply method, IFsrmClassifierModuleImplementation.DoesPropertyValueApply, IFsrmClassifierModuleImplementation::DoesPropertyValueApply, fs.ifsrmclassifiermoduleimplementation_doespropertyvalueapply, fsrm.ifsrmclassifiermoduleimplementation_doespropertyvalueapply, fsrmpipeline/IFsrmClassifierModuleImplementation::DoesPropertyValueApply
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
 - IFsrmClassifierModuleImplementation::DoesPropertyValueApply
 - fsrmpipeline/IFsrmClassifierModuleImplementation::DoesPropertyValueApply
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
 - IFsrmClassifierModuleImplementation.DoesPropertyValueApply
---

# IFsrmClassifierModuleImplementation::DoesPropertyValueApply


## -description

Queries  the classifier to find out whether the specified property value applies to the file most recently specified by the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-onbeginfile">IFsrmClassifierModuleImplementation::OnBeginFile</a> method.

## -parameters

### -param property [in]

Name of the property to query.

### -param value [in]

Value of the property to check in the query.

### -param applyValue [out]

Is <b>VARIANT_TRUE</b> if the property applies; otherwise, <b>VARIANT_FALSE</b>.

### -param idRule [in]

The identifier of the rule object associated with the property value being queried. This rule object is in the rule collection passed in by a previous call to the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-userulesanddefinitions">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a> method. The rule object can also be obtained by using this identifier in a call to the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-getbyid">IFsrmCollection::GetById</a> method on this collection.

### -param idPropDef [in]

The identifier of the property definition object that corresponds to the property being queried. This property definition object is in the property definition collection passed in by a previous call to the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-userulesanddefinitions">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a> method. The property definition object can also be obtained by using this identifier in a call to the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-getbyid">IFsrmCollection::GetById</a> method on this collection.

## -returns

The method returns the following return values. Implementers should return an <b>HRESULT</b> error code for any other errors.

## -remarks

This method is called if the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduledefinition-get_needsexplicitvalue">IFsrmClassifierModuleDefinition::NeedsExplicitValue</a> property of the classifier's module definition is <b>VARIANT_FALSE</b>.

The identifiers passed in the <i>idRule</i> and <i>idPropDef</i> parameters can be used by the classifier implementation to determine whether the property value applies to the file. For classifiers that require the associated rule and/or property definition to make the determination, it is suggested that implementers cache the corresponding collections passed to them during <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-userulesanddefinitions">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a>.

If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>