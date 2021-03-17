---
UID: NF:fsrmreports.IFsrmFileManagementJob.DeleteNotification
title: IFsrmFileManagementJob::DeleteNotification (fsrmreports.h)
description: Deletes a notification value from the file management job's list of notifications.
helpviewer_keywords: ["DeleteNotification","DeleteNotification method [File Server Resource Manager]","DeleteNotification method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","DeleteNotification method","IFsrmFileManagementJob.DeleteNotification","IFsrmFileManagementJob::DeleteNotification","fs.ifsrmfilemanagementjob_deletenotification","fsrm.ifsrmfilemanagementjob_deletenotification","fsrmreports/IFsrmFileManagementJob::DeleteNotification"]
old-location: fsrm\ifsrmfilemanagementjob_deletenotification.htm
tech.root: fsrm
ms.assetid: d21e289a-5062-4897-9479-3408589db11f
ms.date: 12/05/2018
ms.keywords: DeleteNotification, DeleteNotification method [File Server Resource Manager], DeleteNotification method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],DeleteNotification method, IFsrmFileManagementJob.DeleteNotification, IFsrmFileManagementJob::DeleteNotification, fs.ifsrmfilemanagementjob_deletenotification, fsrm.ifsrmfilemanagementjob_deletenotification, fsrmreports/IFsrmFileManagementJob::DeleteNotification
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
 - IFsrmFileManagementJob::DeleteNotification
 - fsrmreports/IFsrmFileManagementJob::DeleteNotification
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
 - IFsrmFileManagementJob.DeleteNotification
---

# IFsrmFileManagementJob::DeleteNotification


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Deletes a notification value from the file management job's list of notifications.

## -parameters

### -param days [in]

The notification value to delete.

## -returns

The method returns the following return values.

## -remarks

Deleting the notification also deletes its associated actions.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-addnotification">IFsrmFileManagementJob::AddNotification</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-modifynotification">IFsrmFileManagementJob::ModifyNotification</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_notifications">IFsrmFileManagementJob::Notifications</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>