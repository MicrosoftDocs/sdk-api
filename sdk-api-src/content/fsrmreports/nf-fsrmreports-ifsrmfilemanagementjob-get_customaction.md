---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_CustomAction
title: IFsrmFileManagementJob::get_CustomAction (fsrmreports.h)
description: The action to execute when all the conditions are met.
helpviewer_keywords: ["CustomAction property [File Server Resource Manager]","CustomAction property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","CustomAction property","IFsrmFileManagementJob.CustomAction","IFsrmFileManagementJob.get_CustomAction","IFsrmFileManagementJob::CustomAction","IFsrmFileManagementJob::get_CustomAction","fs.ifsrmfilemanagementjob_customaction","fsrm.ifsrmfilemanagementjob_customaction","fsrmreports/IFsrmFileManagementJob::CustomAction","fsrmreports/IFsrmFileManagementJob::get_CustomAction","get_CustomAction"]
old-location: fsrm\ifsrmfilemanagementjob_customaction.htm
tech.root: fsrm
ms.assetid: 25014b2d-4f08-45bb-a4c4-d8ab72dc53b1
ms.date: 12/05/2018
ms.keywords: CustomAction property [File Server Resource Manager], CustomAction property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CustomAction property, IFsrmFileManagementJob.CustomAction, IFsrmFileManagementJob.get_CustomAction, IFsrmFileManagementJob::CustomAction, IFsrmFileManagementJob::get_CustomAction, fs.ifsrmfilemanagementjob_customaction, fsrm.ifsrmfilemanagementjob_customaction, fsrmreports/IFsrmFileManagementJob::CustomAction, fsrmreports/IFsrmFileManagementJob::get_CustomAction, get_CustomAction
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
 - IFsrmFileManagementJob::get_CustomAction
 - fsrmreports/IFsrmFileManagementJob::get_CustomAction
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
 - IFsrmFileManagementJob.CustomAction
 - IFsrmFileManagementJob.get_CustomAction
---

# IFsrmFileManagementJob::get_CustomAction


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The action to execute when all the conditions are met.

This property is read-only.

## -parameters

## -remarks

To create the custom action, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createcustomaction">IFsrmFileManagementJob::CreateCustomAction</a> 
    method.

For a list of macros supported, perform a "get" operation on the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariables">IFsrmFileManagementJobManager::ActionVariables</a> 
    and 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariabledescriptions">IFsrmFileManagementJobManager::ActionVariableDescriptions</a> 
    properties.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>