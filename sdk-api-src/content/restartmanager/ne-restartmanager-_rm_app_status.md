---
UID: NE:restartmanager._RM_APP_STATUS
title: "_RM_APP_STATUS"
author: windows-sdk-content
description: Describes the current status of an application that is acted upon by the Restart Manager.
old-location: rstmgr\rm_app_status.htm
old-project: rstmgr
ms.assetid: cb3fe44b-1049-4189-a19a-b5a8fec6daf8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RM_APP_STATUS, RmStatusErrorOnRestart, RmStatusErrorOnStop, RmStatusRestartMasked, RmStatusRestarted, RmStatusRunning, RmStatusShutdownMasked, RmStatusStopped, RmStatusStoppedOther, RmStatusUnknown, _RM_APP_STATUS, _RM_APP_STATUS enumeration [Restart Mgr], restartmanager/RmStatusErrorOnRestart, restartmanager/RmStatusErrorOnStop, restartmanager/RmStatusRestartMasked, restartmanager/RmStatusRestarted, restartmanager/RmStatusRunning, restartmanager/RmStatusShutdownMasked, restartmanager/RmStatusStopped, restartmanager/RmStatusStoppedOther, restartmanager/RmStatusUnknown, restartmanager/_RM_APP_STATUS, rstmgr.rm_app_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: RM_APP_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_APP_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _RM_APP_STATUS enumeration


## -description


Describes the current status of an application that is acted upon by the Restart Manager.


## -enum-fields




### -field RmStatusUnknown

The application is in a state that is not described by any other enumerated state.


### -field RmStatusRunning

The application is currently running.


### -field RmStatusStopped

The Restart Manager has stopped the application.


### -field RmStatusStoppedOther

An action outside the Restart Manager has stopped the application.


### -field RmStatusRestarted

The Restart Manager has restarted the application.


### -field RmStatusErrorOnStop

The Restart Manager encountered an error when stopping the application.


### -field RmStatusErrorOnRestart

The Restart Manager encountered an error when restarting the application.


### -field RmStatusShutdownMasked

Shutdown is masked by a filter.


### -field RmStatusRestartMasked

Restart is masked by a filter.


## -remarks



The constants  of <b>RM_APP_STATUS</b> can be combined with OR operators. The combination describes the history of actions taken by Restart Manager on the application.




## -see-also




<a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a>
 

 

