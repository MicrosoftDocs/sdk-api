---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreatePropertyCondition
title: IFsrmFileManagementJob::CreatePropertyCondition (fsrmreports.h)
description: Creates a new property condition and adds it to the collection of property conditions.
helpviewer_keywords: ["CreatePropertyCondition","CreatePropertyCondition method [File Server Resource Manager]","CreatePropertyCondition method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","CreatePropertyCondition method","IFsrmFileManagementJob.CreatePropertyCondition","IFsrmFileManagementJob::CreatePropertyCondition","fs.ifsrmfilemanagementjob_createpropertycondition","fsrm.ifsrmfilemanagementjob_createpropertycondition","fsrmreports/IFsrmFileManagementJob::CreatePropertyCondition"]
old-location: fsrm\ifsrmfilemanagementjob_createpropertycondition.htm
tech.root: fsrm
ms.assetid: 1b264e9c-4ba0-4de2-acdc-94338519c5af
ms.date: 12/05/2018
ms.keywords: CreatePropertyCondition, CreatePropertyCondition method [File Server Resource Manager], CreatePropertyCondition method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CreatePropertyCondition method, IFsrmFileManagementJob.CreatePropertyCondition, IFsrmFileManagementJob::CreatePropertyCondition, fs.ifsrmfilemanagementjob_createpropertycondition, fsrm.ifsrmfilemanagementjob_createpropertycondition, fsrmreports/IFsrmFileManagementJob::CreatePropertyCondition
req.header: fsrmreports.h
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
 - IFsrmFileManagementJob::CreatePropertyCondition
 - fsrmreports/IFsrmFileManagementJob::CreatePropertyCondition
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
 - IFsrmFileManagementJob.CreatePropertyCondition
---

# IFsrmFileManagementJob::CreatePropertyCondition


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Creates a new property condition and adds it to the collection of property conditions.

## -parameters

### -param name [in]

The name of the property definition that the condition applies to. To enumerate the defined property 
      definitions, call the 
      <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a> 
      method.

### -param propertyCondition [out]

An <a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmpropertycondition">IFsrmPropertyCondition</a> interface that you 
      use to define the newly created property condition.

## -returns

The method returns the following return values.

## -remarks

To enumerate the collection of property conditions associated with the job, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">PropertyConditions</a> 
    property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>