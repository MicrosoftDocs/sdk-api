---
UID: NE:mobsync._tagSYNCMGRFLAG
title: SYNCMGRFLAG (mobsync.h)
description: The SYNCMGRFLAG enumeration values are used in the ISyncMgrSynchronize::Initialize method to indicate how the synchronization event was initiated.
helpviewer_keywords: ["SYNCMGRFLAG","SYNCMGRFLAG enumeration [Windows Shell]","SYNCMGRFLAG_CONNECT","SYNCMGRFLAG_EVENTMASK","SYNCMGRFLAG_IDLE","SYNCMGRFLAG_INVOKE","SYNCMGRFLAG_MANUAL","SYNCMGRFLAG_MAYBOTHERUSER","SYNCMGRFLAG_PENDINGDISCONNECT","SYNCMGRFLAG_SCHEDULED","SYNCMGRFLAG_SETTINGS","mobsync/SYNCMGRFLAG","mobsync/SYNCMGRFLAG_CONNECT","mobsync/SYNCMGRFLAG_EVENTMASK","mobsync/SYNCMGRFLAG_IDLE","mobsync/SYNCMGRFLAG_INVOKE","mobsync/SYNCMGRFLAG_MANUAL","mobsync/SYNCMGRFLAG_MAYBOTHERUSER","mobsync/SYNCMGRFLAG_PENDINGDISCONNECT","mobsync/SYNCMGRFLAG_SCHEDULED","mobsync/SYNCMGRFLAG_SETTINGS","shell.syncmgr_syncmgrflag","syncmgr.syncmgrflag"]
old-location: shell\syncmgr_syncmgrflag.htm
tech.root: shell
ms.assetid: b1a60a6b-b4f8-4c89-853b-5a5584c415e9
ms.date: 12/05/2018
ms.keywords: SYNCMGRFLAG, SYNCMGRFLAG enumeration [Windows Shell], SYNCMGRFLAG_CONNECT, SYNCMGRFLAG_EVENTMASK, SYNCMGRFLAG_IDLE, SYNCMGRFLAG_INVOKE, SYNCMGRFLAG_MANUAL, SYNCMGRFLAG_MAYBOTHERUSER, SYNCMGRFLAG_PENDINGDISCONNECT, SYNCMGRFLAG_SCHEDULED, SYNCMGRFLAG_SETTINGS, mobsync/SYNCMGRFLAG, mobsync/SYNCMGRFLAG_CONNECT, mobsync/SYNCMGRFLAG_EVENTMASK, mobsync/SYNCMGRFLAG_IDLE, mobsync/SYNCMGRFLAG_INVOKE, mobsync/SYNCMGRFLAG_MANUAL, mobsync/SYNCMGRFLAG_MAYBOTHERUSER, mobsync/SYNCMGRFLAG_PENDINGDISCONNECT, mobsync/SYNCMGRFLAG_SCHEDULED, mobsync/SYNCMGRFLAG_SETTINGS, shell.syncmgr_syncmgrflag, syncmgr.syncmgrflag
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SYNCMGRFLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRFLAG
 - mobsync/_tagSYNCMGRFLAG
 - SYNCMGRFLAG
 - mobsync/SYNCMGRFLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRFLAG
---

# SYNCMGRFLAG enumeration


## -description

The <b>SYNCMGRFLAG</b> enumeration values are used in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a> method to indicate how the synchronization event was initiated.

## -enum-fields

### -field SYNCMGRFLAG_CONNECT:0x1

Synchronization was initiated by a network connect event.

### -field SYNCMGRFLAG_PENDINGDISCONNECT:0x2

Synchronization was initiated by a pending network disconnect event.

### -field SYNCMGRFLAG_MANUAL:0x3

Synchronization was initiated manually by the end user.

### -field SYNCMGRFLAG_IDLE:0x4

Synchronization was programmatically invoked.

### -field SYNCMGRFLAG_INVOKE:0x5

Synchronization was programmatically invoked.

### -field SYNCMGRFLAG_SCHEDULED:0x6

Synchronization was initiated by a scheduled update event.

### -field SYNCMGRFLAG_EVENTMASK:0xff

Synchronization mask value.

### -field SYNCMGRFLAG_SETTINGS:0x100

Synchronization was initiated for configuration purposes only in the <b>System Properties</b> dialog box.

### -field SYNCMGRFLAG_MAYBOTHERUSER:0x200

Interaction with the user is permitted. The application is allowed to show user interface elements and interact with the user. If this flag is not set, the application must not display any user interface elements other than using the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> interface. If an application cannot complete the synchronization without displaying user interface elements and this flag is not set, the application fails the synchronization.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a>
