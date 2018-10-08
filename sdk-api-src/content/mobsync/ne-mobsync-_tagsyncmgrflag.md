---
UID: NE:mobsync._tagSYNCMGRFLAG
title: "_tagSYNCMGRFLAG"
author: windows-sdk-content
description: The SYNCMGRFLAG enumeration values are used in the ISyncMgrSynchronize::Initialize method to indicate how the synchronization event was initiated.
old-location: shell\syncmgr_syncmgrflag.htm
tech.root: shell
ms.assetid: b1a60a6b-b4f8-4c89-853b-5a5584c415e9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SYNCMGRFLAG, SYNCMGRFLAG enumeration [Windows Shell], SYNCMGRFLAG_CONNECT, SYNCMGRFLAG_EVENTMASK, SYNCMGRFLAG_IDLE, SYNCMGRFLAG_INVOKE, SYNCMGRFLAG_MANUAL, SYNCMGRFLAG_MAYBOTHERUSER, SYNCMGRFLAG_PENDINGDISCONNECT, SYNCMGRFLAG_SCHEDULED, SYNCMGRFLAG_SETTINGS, _tagSYNCMGRFLAG, mobsync/SYNCMGRFLAG, mobsync/SYNCMGRFLAG_CONNECT, mobsync/SYNCMGRFLAG_EVENTMASK, mobsync/SYNCMGRFLAG_IDLE, mobsync/SYNCMGRFLAG_INVOKE, mobsync/SYNCMGRFLAG_MANUAL, mobsync/SYNCMGRFLAG_MAYBOTHERUSER, mobsync/SYNCMGRFLAG_PENDINGDISCONNECT, mobsync/SYNCMGRFLAG_SCHEDULED, mobsync/SYNCMGRFLAG_SETTINGS, shell.syncmgr_syncmgrflag, syncmgr.syncmgrflag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRFLAG
product: Windows
targetos: Windows
req.typenames: SYNCMGRFLAG
req.redist: 
---

# _tagSYNCMGRFLAG enumeration


## -description


The <b>SYNCMGRFLAG</b> enumeration values are used in the <a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a> method to indicate how the synchronization event was initiated.


## -enum-fields




### -field SYNCMGRFLAG_CONNECT

Synchronization was initiated by a network connect event.


### -field SYNCMGRFLAG_PENDINGDISCONNECT

Synchronization was initiated by a pending network disconnect event.


### -field SYNCMGRFLAG_MANUAL

Synchronization was initiated manually by the end user.


### -field SYNCMGRFLAG_IDLE

Synchronization was programmatically invoked.


### -field SYNCMGRFLAG_INVOKE

Synchronization was programmatically invoked.


### -field SYNCMGRFLAG_SCHEDULED

Synchronization was initiated by a scheduled update event.


### -field SYNCMGRFLAG_EVENTMASK

Synchronization mask value.


### -field SYNCMGRFLAG_SETTINGS

Synchronization was initiated for configuration purposes only in the <b>System Properties</b> dialog box.


### -field SYNCMGRFLAG_MAYBOTHERUSER

Interaction with the user is permitted. The application is allowed to show user interface elements and interact with the user. If this flag is not set, the application must not display any user interface elements other than using the <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface. If an application cannot complete the synchronization without displaying user interface elements and this flag is not set, the application fails the synchronization.


## -see-also




<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>
 

 

