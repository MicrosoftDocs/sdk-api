---
UID: NF:fsrmreports.IFsrmFileManagementJob.DeleteNotification
title: IFsrmFileManagementJob::DeleteNotification
author: windows-sdk-content
description: Deletes a notification value from the file management job's list of notifications.
old-location: fsrm\ifsrmfilemanagementjob_deletenotification.htm
tech.root: Fsrm
ms.assetid: d21e289a-5062-4897-9479-3408589db11f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteNotification, DeleteNotification method [File Server Resource Manager], DeleteNotification method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DeleteNotification method, IFsrmFileManagementJob.DeleteNotification, IFsrmFileManagementJob::DeleteNotification, fs.ifsrmfilemanagementjob_deletenotification, fsrm.ifsrmfilemanagementjob_deletenotification, fsrmreports/IFsrmFileManagementJob::DeleteNotification
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
 - IFsrmFileManagementJob.DeleteNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::DeleteNotification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Deletes a notification value from the file management job's list of notifications.


## -parameters




### -param days [in]

The notification value to delete.


## -returns



The method returns the following return values.




## -remarks



Deleting the notification also deletes its associated actions.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/95b41aa0-44c9-41a2-8132-6aecc4685243">IFsrmFileManagementJob::AddNotification</a>



<a href="https://msdn.microsoft.com/f2b26ed7-5bbc-4b34-ae11-7fcdb621a55b">IFsrmFileManagementJob::ModifyNotification</a>



<a href="https://msdn.microsoft.com/f0aee951-12f3-40d0-bbf4-c72af117952f">IFsrmFileManagementJob::Notifications</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

