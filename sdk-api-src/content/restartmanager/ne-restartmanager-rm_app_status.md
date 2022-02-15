---
UID: NE:restartmanager._RM_APP_STATUS
title: RM_APP_STATUS (restartmanager.h)
description: Describes the current status of an application that is acted upon by the Restart Manager.
helpviewer_keywords: ["RM_APP_STATUS","RmStatusErrorOnRestart","RmStatusErrorOnStop","RmStatusRestartMasked","RmStatusRestarted","RmStatusRunning","RmStatusShutdownMasked","RmStatusStopped","RmStatusStoppedOther","RmStatusUnknown","_RM_APP_STATUS","_RM_APP_STATUS enumeration [Restart Mgr]","restartmanager/RmStatusErrorOnRestart","restartmanager/RmStatusErrorOnStop","restartmanager/RmStatusRestartMasked","restartmanager/RmStatusRestarted","restartmanager/RmStatusRunning","restartmanager/RmStatusShutdownMasked","restartmanager/RmStatusStopped","restartmanager/RmStatusStoppedOther","restartmanager/RmStatusUnknown","restartmanager/_RM_APP_STATUS","rstmgr.rm_app_status"]
old-location: rstmgr\rm_app_status.htm
tech.root: rstmgr
ms.assetid: cb3fe44b-1049-4189-a19a-b5a8fec6daf8
ms.date: 12/05/2018
ms.keywords: RM_APP_STATUS, RmStatusErrorOnRestart, RmStatusErrorOnStop, RmStatusRestartMasked, RmStatusRestarted, RmStatusRunning, RmStatusShutdownMasked, RmStatusStopped, RmStatusStoppedOther, RmStatusUnknown, _RM_APP_STATUS, _RM_APP_STATUS enumeration [Restart Mgr], restartmanager/RmStatusErrorOnRestart, restartmanager/RmStatusErrorOnStop, restartmanager/RmStatusRestartMasked, restartmanager/RmStatusRestarted, restartmanager/RmStatusRunning, restartmanager/RmStatusShutdownMasked, restartmanager/RmStatusStopped, restartmanager/RmStatusStoppedOther, restartmanager/RmStatusUnknown, restartmanager/_RM_APP_STATUS, rstmgr.rm_app_status
req.header: restartmanager.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: RM_APP_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_APP_STATUS
 - restartmanager/_RM_APP_STATUS
 - RM_APP_STATUS
 - restartmanager/RM_APP_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_APP_STATUS
---

# RM_APP_STATUS enumeration


## -description

Describes the current status of an application that is acted upon by the Restart Manager.

## -enum-fields

### -field RmStatusUnknown:0x0

The application is in a state that is not described by any other enumerated state.

### -field RmStatusRunning:0x1

The application is currently running.

### -field RmStatusStopped:0x2

The Restart Manager has stopped the application.

### -field RmStatusStoppedOther:0x4

An action outside the Restart Manager has stopped the application.

### -field RmStatusRestarted:0x8

The Restart Manager has restarted the application.

### -field RmStatusErrorOnStop:0x10

The Restart Manager encountered an error when stopping the application.

### -field RmStatusErrorOnRestart:0x20

The Restart Manager encountered an error when restarting the application.

### -field RmStatusShutdownMasked:0x40

Shutdown is masked by a filter.

### -field RmStatusRestartMasked:0x80    

Restart is masked by a filter.

## -remarks

The constants  of <b>RM_APP_STATUS</b> can be combined with OR operators. The combination describes the history of actions taken by Restart Manager on the application.

## -see-also

<a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a>
