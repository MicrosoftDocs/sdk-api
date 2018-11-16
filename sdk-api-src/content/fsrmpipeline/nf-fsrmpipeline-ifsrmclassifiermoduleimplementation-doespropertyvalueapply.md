---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.DoesPropertyValueApply
title: IFsrmClassifierModuleImplementation::DoesPropertyValueApply
author: windows-sdk-content
description: Queries the classifier to find out whether the specified property value applies to the file most recently specified by the IFsrmClassifierModuleImplementation::OnBeginFile method.
old-location: fsrm\ifsrmclassifiermoduleimplementation_doespropertyvalueapply.htm
tech.root: Fsrm
ms.assetid: ab42430c-1e30-4576-b6f8-c0488b6230dd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DoesPropertyValueApply, DoesPropertyValueApply method [File Server Resource Manager], DoesPropertyValueApply method [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, IFsrmClassifierModuleImplementation interface [File Server Resource Manager],DoesPropertyValueApply method, IFsrmClassifierModuleImplementation.DoesPropertyValueApply, IFsrmClassifierModuleImplementation::DoesPropertyValueApply, fs.ifsrmclassifiermoduleimplementation_doespropertyvalueapply, fsrm.ifsrmclassifiermoduleimplementation_doespropertyvalueapply, fsrmpipeline/IFsrmClassifierModuleImplementation::DoesPropertyValueApply
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmClassifierModuleImplementation.DoesPropertyValueApply
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmpipeline.h
: 
- IFsrmClassifierModuleImplementation.DoesPropertyValueApply
: 
---

# IFsrmClassifierModuleImplementation::DoesPropertyValueApply


## -description


Queries  the classifier to find out whether the specified property value applies to the file most recently specified by the <a href="https://msdn.microsoft.com/799f26c7-925e-4669-9571-128e10c51e9c">IFsrmClassifierModuleImplementation::OnBeginFile</a> method.


## -parameters




### -param property [in]

Name of the property to query.


### -param value [in]

Value of the property to check in the query.


### -param applyValue [out]

Is <b>VARIANT_TRUE</b> if the property applies; otherwise, <b>VARIANT_FALSE</b>.


### -param idRule [in]

The identifier of the rule object associated with the property value being queried. This rule object is in the rule collection passed in by a previous call to the <a href="https://msdn.microsoft.com/8fbca8c4-7021-4183-b8f7-a32082da17fc">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a> method. The rule object can also be obtained by using this identifier in a call to the <a href="https://msdn.microsoft.com/6d6be809-bfe6-46ad-9156-288da834ff13">IFsrmCollection::GetById</a> method on this collection.


### -param idPropDef [in]

The identifier of the property definition object that corresponds to the property being queried. This property definition object is in the property definition collection passed in by a previous call to the <a href="https://msdn.microsoft.com/8fbca8c4-7021-4183-b8f7-a32082da17fc">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a> method. The property definition object can also be obtained by using this identifier in a call to the <a href="https://msdn.microsoft.com/6d6be809-bfe6-46ad-9156-288da834ff13">IFsrmCollection::GetById</a> method on this collection.


## -returns



The method returns the following return values. Implementers should return an <b>HRESULT</b> error code for any other errors.




## -remarks



This method is called if the <a href="https://msdn.microsoft.com/580542ef-c766-4a39-9dbd-aed2f4a11780">IFsrmClassifierModuleDefinition::NeedsExplicitValue</a> property of the classifier's module definition is <b>VARIANT_FALSE</b>.

The identifiers passed in the <i>idRule</i> and <i>idPropDef</i> parameters can be used by the classifier implementation to determine whether the property value applies to the file. For classifiers that require the associated rule and/or property definition to make the determination, it is suggested that implementers cache the corresponding collections passed to them during <a href="https://msdn.microsoft.com/8fbca8c4-7021-4183-b8f7-a32082da17fc">IFsrmClassifierModuleImplementation::UseRulesAndDefinitions</a>.

If <b>FSRM_E_INCOMPATIBLE_FORMAT</b> or <b>FSRM_E_FILE_ENCRYPTED</b> is returned, FSRM will not indicate that the file has failed classification. If any other error value is returned, FSRM will indicate that the file has failed classification.




## -see-also




<a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a>
 

 

