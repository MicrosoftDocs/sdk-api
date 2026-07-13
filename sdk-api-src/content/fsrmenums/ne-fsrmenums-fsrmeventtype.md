---
UID: NE:fsrmenums._FsrmEventType
title: FsrmEventType (fsrmenums.h)
description: Defines the event types that an event logging action (see FsrmActionType) can log.
helpviewer_keywords: ["FsrmEventType","FsrmEventType enumeration [File Server Resource Manager]","FsrmEventType_Error","FsrmEventType_Information","FsrmEventType_Unknown","FsrmEventType_Warning","fs.fsrmeventtype","fsrm.fsrmeventtype","fsrmenums/FsrmEventType","fsrmenums/FsrmEventType_Error","fsrmenums/FsrmEventType_Information","fsrmenums/FsrmEventType_Unknown","fsrmenums/FsrmEventType_Warning"]
old-location: fsrm\fsrmeventtype.htm
tech.root: fsrm
ms.assetid: 517992e2-ecbe-40bf-b93c-81f509f26162
ms.date: 12/05/2018
ms.keywords: FsrmEventType, FsrmEventType enumeration [File Server Resource Manager], FsrmEventType_Error, FsrmEventType_Information, FsrmEventType_Unknown, FsrmEventType_Warning, fs.fsrmeventtype, fsrm.fsrmeventtype, fsrmenums/FsrmEventType, fsrmenums/FsrmEventType_Error, fsrmenums/FsrmEventType_Information, fsrmenums/FsrmEventType_Unknown, fsrmenums/FsrmEventType_Warning
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
targetos: Windows
req.typenames: FsrmEventType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmEventType
 - fsrmenums/_FsrmEventType
 - FsrmEventType
 - fsrmenums/FsrmEventType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmEventType
---

# FsrmEventType enumeration


## -description

Defines the event types that an event logging action (see 
    <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a>) can log.

## -enum-fields

### -field FsrmEventType_Unknown:0

The event type is unknown. Do not use this flag.

### -field FsrmEventType_Information:1

The event is an information event.

### -field FsrmEventType_Warning:2

The event is a warning event.

### -field FsrmEventType_Error:3

The event is an error event.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioneventlog-get_eventtype">IFsrmActionEventLog::EventType</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>
