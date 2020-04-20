---
UID: NE:restartmanager._RM_REBOOT_REASON
title: RM_REBOOT_REASON (restartmanager.h)
description: Describes the reasons a restart of the system is needed.helpviewer_keywords: ["RM_REBOOT_REASON","RM_REBOOT_REASON enumeration [Restart Mgr]","RmRebootReasonCriticalProcess","RmRebootReasonCriticalService","RmRebootReasonDetectedSelf","RmRebootReasonNone","RmRebootReasonPermissionDenied","RmRebootReasonSessionMismatch","restartmanager/RM_REBOOT_REASON","restartmanager/RmRebootReasonCriticalProcess","restartmanager/RmRebootReasonCriticalService","restartmanager/RmRebootReasonDetectedSelf","restartmanager/RmRebootReasonNone","restartmanager/RmRebootReasonPermissionDenied","restartmanager/RmRebootReasonSessionMismatch","rstmgr.rm_reboot_reason"]
old-location: rstmgr\rm_reboot_reason.htm
tech.root: rstmgr
ms.assetid: f99c1b66-db2f-4520-86cf-19961e511474
ms.date: 12/05/2018
ms.keywords: RM_REBOOT_REASON, RM_REBOOT_REASON enumeration [Restart Mgr], RmRebootReasonCriticalProcess, RmRebootReasonCriticalService, RmRebootReasonDetectedSelf, RmRebootReasonNone, RmRebootReasonPermissionDenied, RmRebootReasonSessionMismatch, restartmanager/RM_REBOOT_REASON, restartmanager/RmRebootReasonCriticalProcess, restartmanager/RmRebootReasonCriticalService, restartmanager/RmRebootReasonDetectedSelf, restartmanager/RmRebootReasonNone, restartmanager/RmRebootReasonPermissionDenied, restartmanager/RmRebootReasonSessionMismatch, rstmgr.rm_reboot_reason
f1_keywords:
- restartmanager/RM_REBOOT_REASON
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- RestartManager.h
api_name:
- RM_REBOOT_REASON
targetos: Windows
req.typenames: RM_REBOOT_REASON
req.redist: 
ms.custom: 19H1
---

# RM_REBOOT_REASON enumeration


## -description


Describes the reasons a restart of the system is needed.


## -enum-fields




### -field RmRebootReasonNone

A system restart is not required.


### -field RmRebootReasonPermissionDenied

The current user does not have
                                            sufficient privileges to shut down one or more processes.


### -field RmRebootReasonSessionMismatch

One or more processes are
                                            running in another Terminal Services session.


### -field RmRebootReasonCriticalProcess

A system restart is needed because one or more processes to be shut down are critical processes.


### -field RmRebootReasonCriticalService

A system restart is needed because one or more services to be shut down are critical services.


### -field RmRebootReasonDetectedSelf

A system restart is needed because the current process must be shut down.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/restartmanager/nf-restartmanager-rmgetlist">RmGetList</a>
 

 

