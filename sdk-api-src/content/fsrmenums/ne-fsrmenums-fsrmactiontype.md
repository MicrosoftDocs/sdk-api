---
UID: NE:fsrmenums._FsrmActionType
title: FsrmActionType (fsrmenums.h)
author: windows-sdk-content
description: Defines the actions that can be triggered in response to a quota or file screen event (for example, a quota is exceeded or a file violates a file screen).
old-location: fsrm\fsrmactiontype.htm
tech.root: fsrm
ms.assetid: 3e34395e-b8e6-4288-a040-dff6cf7f5fe6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmActionType, FsrmActionType enumeration [File Server Resource Manager], FsrmActionType_Command, FsrmActionType_Email, FsrmActionType_EventLog, FsrmActionType_Report, FsrmActionType_Unknown, fs.fsrmactiontype, fsrm.fsrmactiontype, fsrmenums/FsrmActionType, fsrmenums/FsrmActionType_Command, fsrmenums/FsrmActionType_Email, fsrmenums/FsrmActionType_EventLog, fsrmenums/FsrmActionType_Report, fsrmenums/FsrmActionType_Unknown
ms.topic: enum
f1_keywords:
- fsrmenums/FsrmActionType
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- FsrmEnums.h
api_name:
- FsrmActionType
targetos: Windows
req.typenames: FsrmActionType
req.redist: 
ms.custom: 19H1
---

# FsrmActionType enumeration


## -description


Defines the actions that can be triggered in response to a quota or file screen event (for example, a 
    quota is exceeded or a file violates a file screen). A file management job can also trigger the 
    action.


## -enum-fields




### -field FsrmActionType_Unknown

The action is of an unknown type. Do not use this value to specify an action type.


### -field FsrmActionType_EventLog

Log an event to the Application event log.


### -field FsrmActionType_Email

Send an email message.


### -field FsrmActionType_Command

Execute a command or script.


### -field FsrmActionType_Report

Generate a report.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmaccounttype">FsrmAccountType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmeventtype">FsrmEventType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">IFsrmAction::ActionType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-getactionrunlimitinterval">IFsrmSetting::GetActionRunLimitInterval</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-setactionrunlimitinterval">IFsrmSetting::SetActionRunLimitInterval</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>
 

 

