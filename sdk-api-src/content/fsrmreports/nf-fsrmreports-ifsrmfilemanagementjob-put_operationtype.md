---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_OperationType
title: IFsrmFileManagementJob::put_OperationType
author: windows-sdk-content
description: The type of file management job. The type determines the operation to perform on a file when all conditions are met.
old-location: fsrm\ifsrmfilemanagementjob_operationtype.htm
tech.root: fsrm
ms.assetid: 98816ea0-7651-42ef-8893-13c568ed859a
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],OperationType property, IFsrmFileManagementJob.OperationType, IFsrmFileManagementJob.put_OperationType, IFsrmFileManagementJob::OperationType, IFsrmFileManagementJob::get_OperationType, IFsrmFileManagementJob::put_OperationType, OperationType property [File Server Resource Manager], OperationType property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_operationtype, fsrm.ifsrmfilemanagementjob_operationtype, fsrmreports/IFsrmFileManagementJob::OperationType, fsrmreports/IFsrmFileManagementJob::get_OperationType, fsrmreports/IFsrmFileManagementJob::put_OperationType, put_OperationType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::put_OperationType


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The type of file management job. The type determines the operation to perform on a file when all 
    conditions are met.

This property is read/write.


## -parameters


## -remarks



If the type is <b>FsrmFileManagementType_Expiration</b>, FSRM moves the files that meet 
    all the file management job's conditions to the path specified by the 
    <a href="https://msdn.microsoft.com/7c8a2584-23ff-4839-b426-8f5411955746">ExpirationDirectory</a> property 
    when the job is run.

If the type is <b>FsrmFileManagementType_Custom</b>, FSRM executes the custom action 
    specified in the <a href="https://msdn.microsoft.com/25014b2d-4f08-45bb-a4c4-d8ab72dc53b1">CustomAction</a> 
    property for every file that meets all the file management job's conditions when the file management job is 
    run.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

