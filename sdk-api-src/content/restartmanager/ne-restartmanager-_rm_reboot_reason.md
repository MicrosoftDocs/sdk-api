---
UID: NE:restartmanager._RM_REBOOT_REASON
title: "_RM_REBOOT_REASON"
author: windows-sdk-content
description: Describes the reasons a restart of the system is needed.
old-location: rstmgr\rm_reboot_reason.htm
old-project: RstMgr
ms.assetid: f99c1b66-db2f-4520-86cf-19961e511474
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RM_REBOOT_REASON, RM_REBOOT_REASON enumeration [Restart Mgr], RmRebootReasonCriticalProcess, RmRebootReasonCriticalService, RmRebootReasonDetectedSelf, RmRebootReasonNone, RmRebootReasonPermissionDenied, RmRebootReasonSessionMismatch, _RM_REBOOT_REASON, restartmanager/RM_REBOOT_REASON, restartmanager/RmRebootReasonCriticalProcess, restartmanager/RmRebootReasonCriticalService, restartmanager/RmRebootReasonDetectedSelf, restartmanager/RmRebootReasonNone, restartmanager/RmRebootReasonPermissionDenied, restartmanager/RmRebootReasonSessionMismatch, rstmgr.rm_reboot_reason
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: restartmanager.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RM_REBOOT_REASON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_REBOOT_REASON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _RM_REBOOT_REASON enumeration


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




<a href="https://msdn.microsoft.com/de4feea4-2b45-4430-a4b3-8ca26c455e42">RmGetList</a>
 

 

