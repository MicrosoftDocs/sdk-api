---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_OperationType
title: IFsrmFileManagementJob::get_OperationType (fsrmreports.h)
description: The type of file management job. The type determines the operation to perform on a file when all conditions are met. (Get)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","OperationType property","IFsrmFileManagementJob.OperationType","IFsrmFileManagementJob.get_OperationType","IFsrmFileManagementJob::OperationType","IFsrmFileManagementJob::get_OperationType","IFsrmFileManagementJob::put_OperationType","OperationType property [File Server Resource Manager]","OperationType property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_operationtype","fsrm.ifsrmfilemanagementjob_operationtype","fsrmreports/IFsrmFileManagementJob::OperationType","fsrmreports/IFsrmFileManagementJob::get_OperationType","fsrmreports/IFsrmFileManagementJob::put_OperationType","get_OperationType"]
old-location: fsrm\ifsrmfilemanagementjob_operationtype.htm
tech.root: fsrm
ms.assetid: 98816ea0-7651-42ef-8893-13c568ed859a
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],OperationType property, IFsrmFileManagementJob.OperationType, IFsrmFileManagementJob.get_OperationType, IFsrmFileManagementJob::OperationType, IFsrmFileManagementJob::get_OperationType, IFsrmFileManagementJob::put_OperationType, OperationType property [File Server Resource Manager], OperationType property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_operationtype, fsrm.ifsrmfilemanagementjob_operationtype, fsrmreports/IFsrmFileManagementJob::OperationType, fsrmreports/IFsrmFileManagementJob::get_OperationType, fsrmreports/IFsrmFileManagementJob::put_OperationType, get_OperationType
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
 - IFsrmFileManagementJob::get_OperationType
 - fsrmreports/IFsrmFileManagementJob::get_OperationType
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
 - IFsrmFileManagementJob.OperationType
 - IFsrmFileManagementJob.get_OperationType
 - IFsrmFileManagementJob.put_OperationType
---

# IFsrmFileManagementJob::get_OperationType


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The type of file management job. The type determines the operation to perform on a file when all 
    conditions are met.

This property is read/write.

## -parameters

## -remarks

If the type is <b>FsrmFileManagementType_Expiration</b>, FSRM moves the files that meet 
    all the file management job's conditions to the path specified by the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_expirationdirectory">ExpirationDirectory</a> property 
    when the job is run.

If the type is <b>FsrmFileManagementType_Custom</b>, FSRM executes the custom action 
    specified in the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_customaction">CustomAction</a> 
    property for every file that meets all the file management job's conditions when the file management job is 
    run.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
