---
UID: NF:fsrmreports.IFsrmFileManagementJob.ModifyNotification
title: IFsrmFileManagementJob::ModifyNotification (fsrmreports.h)
author: windows-sdk-content
description: Change a notification value in the file management job's list of notifications.
old-location: fsrm\ifsrmfilemanagementjob_modifynotification.htm
tech.root: fsrm
ms.assetid: f2b26ed7-5bbc-4b34-ae11-7fcdb621a55b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],ModifyNotification method, IFsrmFileManagementJob.ModifyNotification, IFsrmFileManagementJob::ModifyNotification, ModifyNotification, ModifyNotification method [File Server Resource Manager], ModifyNotification method [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_modifynotification, fsrm.ifsrmfilemanagementjob_modifynotification, fsrmreports/IFsrmFileManagementJob::ModifyNotification
ms.topic: method
f1_keywords: 
 - "fsrmreports/IFsrmFileManagementJob.ModifyNotification"
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
 - IFsrmFileManagementJob.ModifyNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJob::ModifyNotification


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Change a notification value in the file management job's list of notifications.


## -parameters




### -param days [in]

The notification value to change.


### -param newDays [in]

The new notification value. The value must be unique and cannot be less than zero.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-addnotification">IFsrmFileManagementJob::AddNotification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-deletenotification">IFsrmFileManagementJob::DeleteNotification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_notifications">IFsrmFileManagementJob::Notifications</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
 

 

