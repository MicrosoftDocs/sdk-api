---
UID: NN:fsrmpipeline.IFsrmPropertyDefinition
title: IFsrmPropertyDefinition (fsrmpipeline.h)
description: Defines a property that you want to use to classify files. (IFsrmPropertyDefinition)
helpviewer_keywords: ["IFsrmPropertyDefinition","IFsrmPropertyDefinition interface [File Server Resource Manager]","IFsrmPropertyDefinition interface [File Server Resource Manager]","described","fs.ifsrmpropertydefinition","fsrm.ifsrmpropertydefinition","fsrm/IFsrmPropertyDefinition"]
old-location: fsrm\ifsrmpropertydefinition.htm
tech.root: fsrm
ms.assetid: b85d5df0-a99a-48d2-9bad-3b8c86abea91
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyDefinition, IFsrmPropertyDefinition interface [File Server Resource Manager], IFsrmPropertyDefinition interface [File Server Resource Manager],described, fs.ifsrmpropertydefinition, fsrm.ifsrmpropertydefinition, fsrm/IFsrmPropertyDefinition
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
 - IFsrmPropertyDefinition
 - fsrmpipeline/IFsrmPropertyDefinition
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
 - IFsrmPropertyDefinition
---

# IFsrmPropertyDefinition interface


## -description

Defines a property that you want to use to classify files.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createpropertydefinition">IFsrmClassificationManager::CreatePropertyDefinition</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getpropertydefinition">IFsrmClassificationManager::GetPropertyDefinition</a>
</li>
</ul>

## -remarks

The name and type properties define a unique property; you cannot rename a property or change its type.

You cannot delete a property definition that is referenced by a classification rule or report. The 
    classification rule uses the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationrule-get_propertyaffected">IFsrmRule::PropertyAffected</a> 
    property to reference the property definition.

You cannot delete a property  that is referenced by a file management job property condition. To determine if 
    a property condition is holding a reference, look for property conditions that have the "name" 
    property of the condition equal to the name of the property definition that is being deleted.

Reports use the property definition only as a filter in the report type 
    <b>FsrmReportType_FilesByProperty</b>.


#### Examples

For examples in C# and PowerShell see 
     <a href="/previous-versions/windows/desktop/fsrm/accessing-classification-properties">Accessing Classification Properties</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmproperty">IFsrmProperty</a>
