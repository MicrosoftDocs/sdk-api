---
UID: NF:fsrmreports.IFsrmFileManagementJob.ModifyNotification
title: IFsrmFileManagementJob::ModifyNotification
author: windows-sdk-content
description: Change a notification value in the file management job's list of notifications.
old-location: fsrm\ifsrmfilemanagementjob_modifynotification.htm
old-project: fsrm
ms.assetid: f2b26ed7-5bbc-4b34-ae11-7fcdb621a55b
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],ModifyNotification method, IFsrmFileManagementJob.ModifyNotification, IFsrmFileManagementJob::ModifyNotification, ModifyNotification, ModifyNotification method [File Server Resource Manager], ModifyNotification method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_modifynotification, fsrm.ifsrmfilemanagementjob_modifynotification, fsrmreports/IFsrmFileManagementJob::ModifyNotification
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
 - IFsrmFileManagementJob.ModifyNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::ModifyNotification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Change a notification value in the file management job's list of notifications.


## -parameters




### -param days [in]

The notification value to change.


### -param newDays [in]

The new notification value. The value must be unique and cannot be less than zero.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/95b41aa0-44c9-41a2-8132-6aecc4685243">IFsrmFileManagementJob::AddNotification</a>



<a href="https://msdn.microsoft.com/d21e289a-5062-4897-9479-3408589db11f">IFsrmFileManagementJob::DeleteNotification</a>



<a href="https://msdn.microsoft.com/f0aee951-12f3-40d0-bbf4-c72af117952f">IFsrmFileManagementJob::Notifications</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

