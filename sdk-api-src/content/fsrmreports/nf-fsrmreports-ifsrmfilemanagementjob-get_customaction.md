---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_CustomAction
title: IFsrmFileManagementJob::get_CustomAction
author: windows-sdk-content
description: The action to execute when all the conditions are met.
old-location: fsrm\ifsrmfilemanagementjob_customaction.htm
old-project: Fsrm
ms.assetid: 25014b2d-4f08-45bb-a4c4-d8ab72dc53b1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CustomAction property [File Server Resource Manager], CustomAction property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CustomAction property, IFsrmFileManagementJob.CustomAction, IFsrmFileManagementJob.get_CustomAction, IFsrmFileManagementJob::CustomAction, IFsrmFileManagementJob::get_CustomAction, fs.ifsrmfilemanagementjob_customaction, fsrm.ifsrmfilemanagementjob_customaction, fsrmreports/IFsrmFileManagementJob::CustomAction, fsrmreports/IFsrmFileManagementJob::get_CustomAction, get_CustomAction
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::get_CustomAction


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

The action to execute when all the conditions are met.

This property is read-only.


## -parameters


## -remarks



To create the custom action, call the 
    <a href="https://msdn.microsoft.com/886992bd-ca0b-4f21-8036-39703c7c99ba">IFsrmFileManagementJob::CreateCustomAction</a> 
    method.

For a list of macros supported, perform a "get" operation on the 
    <a href="https://msdn.microsoft.com/222c826f-0ade-4e5d-be2e-5c0dfa8758d0">IFsrmFileManagementJobManager::ActionVariables</a> 
    and 
    <a href="https://msdn.microsoft.com/d8e625b2-5fdd-4e7e-8c20-ad6e3e21a918">IFsrmFileManagementJobManager::ActionVariableDescriptions</a> 
    properties.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

