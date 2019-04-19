---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreateNotificationAction
title: IFsrmFileManagementJob::CreateNotificationAction (fsrmreports.h)
author: windows-sdk-content
description: Creates a notification action and associates it with the notification value.
old-location: fsrm\ifsrmfilemanagementjob_createnotificationaction.htm
tech.root: fsrm
ms.assetid: d0cb2ac1-842c-4ebb-adac-8298a0e0beed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateNotificationAction, CreateNotificationAction method [File Server Resource Manager], CreateNotificationAction method [File Server Resource Manager],IFsrmFileManagementJob interface, FsrmActionType_Command, FsrmActionType_Email, FsrmActionType_EventLog, IFsrmFileManagementJob interface [File Server Resource Manager],CreateNotificationAction method, IFsrmFileManagementJob.CreateNotificationAction, IFsrmFileManagementJob::CreateNotificationAction, fs.ifsrmfilemanagementjob_createnotificationaction, fsrm.ifsrmfilemanagementjob_createnotificationaction, fsrmreports/IFsrmFileManagementJob::CreateNotificationAction
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
 - IFsrmFileManagementJob.CreateNotificationAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJob::CreateNotificationAction


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Creates a notification action and associates it with the notification value.


## -parameters




### -param days [in]

The notification value to associate with the action.


### -param actionType [in]

The action to perform when the notification period is reached, enumerated by the 
      <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmActionType_Report</b> type is not valid for this method.</div>
<div> </div>


#### FsrmActionType_EventLog (1)

Log an event to the Application event log.



#### FsrmActionType_Email (2)

Send an email message.



#### FsrmActionType_Command (3)

Execute a command or script.


### -param action [out]

An <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface of the newly created action. 
      Query the interface for the action interface that you specified in the <i>actionType</i> 
      parameter. For example, if the action type is <b>FsrmActionType_Command</b>, query the 
      interface for the <a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a> interface.


## -returns



The method returns the following return values.




## -remarks



You can specify up to three unique actions for each notification value.

The action is deleted when the notification is deleted.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/cfb58db2-39af-434e-95e2-abbd21f4487a">IFsrmFileManagementJob::EnumNotificationActions</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

