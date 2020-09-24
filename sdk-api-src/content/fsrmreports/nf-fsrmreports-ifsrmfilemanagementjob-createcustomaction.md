---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreateCustomAction
title: IFsrmFileManagementJob::CreateCustomAction (fsrmreports.h)
description: Creates a custom action object.
helpviewer_keywords: ["CreateCustomAction","CreateCustomAction method [File Server Resource Manager]","CreateCustomAction method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","CreateCustomAction method","IFsrmFileManagementJob.CreateCustomAction","IFsrmFileManagementJob::CreateCustomAction","fs.ifsrmfilemanagementjob_createcustomaction","fsrm.ifsrmfilemanagementjob_createcustomaction","fsrmreports/IFsrmFileManagementJob::CreateCustomAction"]
old-location: fsrm\ifsrmfilemanagementjob_createcustomaction.htm
tech.root: fsrm
ms.assetid: 886992bd-ca0b-4f21-8036-39703c7c99ba
ms.date: 12/05/2018
ms.keywords: CreateCustomAction, CreateCustomAction method [File Server Resource Manager], CreateCustomAction method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CreateCustomAction method, IFsrmFileManagementJob.CreateCustomAction, IFsrmFileManagementJob::CreateCustomAction, fs.ifsrmfilemanagementjob_createcustomaction, fsrm.ifsrmfilemanagementjob_createcustomaction, fsrmreports/IFsrmFileManagementJob::CreateCustomAction
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
 - IFsrmFileManagementJob::CreateCustomAction
 - fsrmreports/IFsrmFileManagementJob::CreateCustomAction
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
 - IFsrmFileManagementJob.CreateCustomAction
---

# IFsrmFileManagementJob::CreateCustomAction


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Creates a custom action object.

## -parameters

### -param customAction [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a> interface that you can use 
      to specify a custom action to perform if the job's property conditions are met.

## -returns

The method returns the following return values. Implementers should return an 
      <b>HRESULT</b> error code for any other errors.

## -remarks

To get the custom action, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_customaction">CustomAction</a> property.

Create a custom action only if the job's 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_operationtype">OperationType</a> is set to 
    <b>FsrmFileManagementType_Custom</b>.

For a list of macros supported, perform a "get" operation on the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariables">IFsrmFileManagementJobManager::ActionVariables</a> 
    and 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariabledescriptions">IFsrmFileManagementJobManager::ActionVariableDescriptions</a> 
    properties.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_arguments">IFsrmActionCommand::Arguments</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>