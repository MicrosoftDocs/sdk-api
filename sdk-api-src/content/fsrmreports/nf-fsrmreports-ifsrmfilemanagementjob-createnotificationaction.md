---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreateNotificationAction
title: IFsrmFileManagementJob::CreateNotificationAction (fsrmreports.h)
description: Creates a notification action and associates it with the notification value.
helpviewer_keywords: ["CreateNotificationAction","CreateNotificationAction method [File Server Resource Manager]","CreateNotificationAction method [File Server Resource Manager]","IFsrmFileManagementJob interface","FsrmActionType_Command","FsrmActionType_Email","FsrmActionType_EventLog","IFsrmFileManagementJob interface [File Server Resource Manager]","CreateNotificationAction method","IFsrmFileManagementJob.CreateNotificationAction","IFsrmFileManagementJob::CreateNotificationAction","fs.ifsrmfilemanagementjob_createnotificationaction","fsrm.ifsrmfilemanagementjob_createnotificationaction","fsrmreports/IFsrmFileManagementJob::CreateNotificationAction"]
old-location: fsrm\ifsrmfilemanagementjob_createnotificationaction.htm
tech.root: fsrm
ms.assetid: d0cb2ac1-842c-4ebb-adac-8298a0e0beed
ms.date: 12/05/2018
ms.keywords: CreateNotificationAction, CreateNotificationAction method [File Server Resource Manager], CreateNotificationAction method [File Server Resource Manager],IFsrmFileManagementJob interface, FsrmActionType_Command, FsrmActionType_Email, FsrmActionType_EventLog, IFsrmFileManagementJob interface [File Server Resource Manager],CreateNotificationAction method, IFsrmFileManagementJob.CreateNotificationAction, IFsrmFileManagementJob::CreateNotificationAction, fs.ifsrmfilemanagementjob_createnotificationaction, fsrm.ifsrmfilemanagementjob_createnotificationaction, fsrmreports/IFsrmFileManagementJob::CreateNotificationAction
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
 - IFsrmFileManagementJob::CreateNotificationAction
 - fsrmreports/IFsrmFileManagementJob::CreateNotificationAction
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
 - IFsrmFileManagementJob.CreateNotificationAction
---

# IFsrmFileManagementJob::CreateNotificationAction


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Creates a notification action and associates it with the notification value.

## -parameters

### -param days [in]

The notification value to associate with the action.

### -param actionType [in]

The action to perform when the notification period is reached, enumerated by the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmActionType_Report</b> type is not valid for this method.</div>
<div> </div>


#### FsrmActionType_EventLog (1)

Log an event to the Application event log.



#### FsrmActionType_Email (2)

Send an email message.



#### FsrmActionType_Command (3)

Execute a command or script.

### -param action [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface of the newly created action. 
      Query the interface for the action interface that you specified in the <i>actionType</i> 
      parameter. For example, if the action type is <b>FsrmActionType_Command</b>, query the 
      interface for the <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a> interface.

## -returns

The method returns the following return values.

## -remarks

You can specify up to three unique actions for each notification value.

The action is deleted when the notification is deleted.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-enumnotificationactions">IFsrmFileManagementJob::EnumNotificationActions</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>