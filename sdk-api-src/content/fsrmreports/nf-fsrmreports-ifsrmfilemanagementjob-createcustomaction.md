---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreateCustomAction
title: IFsrmFileManagementJob::CreateCustomAction
author: windows-sdk-content
description: Creates a custom action object.
old-location: fsrm\ifsrmfilemanagementjob_createcustomaction.htm
tech.root: fsrm
ms.assetid: 886992bd-ca0b-4f21-8036-39703c7c99ba
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: CreateCustomAction, CreateCustomAction method [File Server Resource Manager], CreateCustomAction method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CreateCustomAction method, IFsrmFileManagementJob.CreateCustomAction, IFsrmFileManagementJob::CreateCustomAction, fs.ifsrmfilemanagementjob_createcustomaction, fsrm.ifsrmfilemanagementjob_createcustomaction, fsrmreports/IFsrmFileManagementJob::CreateCustomAction
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
 - IFsrmFileManagementJob.CreateCustomAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::CreateCustomAction


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Creates a custom action object.


## -parameters




### -param customAction [out]

An <a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a> interface that you can use 
      to specify a custom action to perform if the job's property conditions are met.


## -returns



The method returns the following return values. Implementers should return an 
      <b>HRESULT</b> error code for any other errors.




## -remarks



To get the custom action, access the 
    <a href="https://msdn.microsoft.com/25014b2d-4f08-45bb-a4c4-d8ab72dc53b1">CustomAction</a> property.

Create a custom action only if the job's 
    <a href="https://msdn.microsoft.com/98816ea0-7651-42ef-8893-13c568ed859a">OperationType</a> is set to 
    <b>FsrmFileManagementType_Custom</b>.

For a list of macros supported, perform a "get" operation on the 
    <a href="https://msdn.microsoft.com/222c826f-0ade-4e5d-be2e-5c0dfa8758d0">IFsrmFileManagementJobManager::ActionVariables</a> 
    and 
    <a href="https://msdn.microsoft.com/d8e625b2-5fdd-4e7e-8c20-ad6e3e21a918">IFsrmFileManagementJobManager::ActionVariableDescriptions</a> 
    properties.




## -see-also




<a href="https://msdn.microsoft.com/2ffc8753-3a63-4619-936d-f2f4d2362508">IFsrmActionCommand::Arguments</a>



<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

