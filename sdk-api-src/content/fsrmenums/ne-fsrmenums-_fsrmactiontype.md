---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FsrmActionType enumeration


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




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/8df04b24-e3dd-46ee-8d06-6a3763946fbe">FsrmAccountType</a>



<a href="https://msdn.microsoft.com/517992e2-ecbe-40bf-b93c-81f509f26162">FsrmEventType</a>



<a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">IFsrmAction::ActionType</a>



<a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a>



<a href="https://msdn.microsoft.com/1d627e07-fa8c-4c22-acba-c08767b8ebaa">IFsrmFileScreenBase::CreateAction</a>



<a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">IFsrmQuotaBase::CreateThresholdAction</a>



<a href="https://msdn.microsoft.com/cbcd5532-4077-4a5c-94d4-e1fb636e6dda">IFsrmSetting::GetActionRunLimitInterval</a>



<a href="https://msdn.microsoft.com/4cd4d583-2906-4ba0-b113-c21db143dec2">IFsrmSetting::SetActionRunLimitInterval</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>
 

 

