---
UID: NE:fsrmenums._FsrmEventType
title: "_FsrmEventType"
author: windows-sdk-content
description: Defines the event types that an event logging action (see FsrmActionType) can log.
old-location: fsrm\fsrmeventtype.htm
old-project: fsrm
ms.assetid: 517992e2-ecbe-40bf-b93c-81f509f26162
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FsrmEventType, FsrmEventType enumeration [File Server Resource Manager], FsrmEventType_Error, FsrmEventType_Information, FsrmEventType_Unknown, FsrmEventType_Warning, _FsrmEventType, fs.fsrmeventtype, fsrm.fsrmeventtype, fsrmenums/FsrmEventType, fsrmenums/FsrmEventType_Error, fsrmenums/FsrmEventType_Information, fsrmenums/FsrmEventType_Unknown, fsrmenums/FsrmEventType_Warning
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmEventType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmEventType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmEventType enumeration


## -description


Defines the event types that an event logging action (see 
    <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a>) can log.


## -enum-fields




### -field FsrmEventType_Unknown

The event type is unknown. Do not use this flag.


### -field FsrmEventType_Information

The event is an information event.


### -field FsrmEventType_Warning

The event is a warning event.


### -field FsrmEventType_Error

The event is an error event.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/eb76fa86-2d82-46a5-ae76-c2f00f812e48">IFsrmActionEventLog::EventType</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>
 

 

