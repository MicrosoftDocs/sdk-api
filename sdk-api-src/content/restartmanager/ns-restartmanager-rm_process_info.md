---
UID: NS:restartmanager._RM_PROCESS_INFO
title: RM_PROCESS_INFO (restartmanager.h)
description: Describes an application that is to be registered with the Restart Manager.
helpviewer_keywords: ["*PRM_PROCESS_INFO","RM_PROCESS_INFO","RM_PROCESS_INFO structure [Restart Mgr]","restartmanager/_RM_PROCESS_INFO","rstmgr.rm_process_info"]
old-location: rstmgr\rm_process_info.htm
tech.root: rstmgr
ms.assetid: 27e593f9-8ff0-4de4-87ca-7fa5f324468a
ms.date: 12/05/2018
ms.keywords: '*PRM_PROCESS_INFO, RM_PROCESS_INFO, RM_PROCESS_INFO structure [Restart Mgr], restartmanager/_RM_PROCESS_INFO, rstmgr.rm_process_info'
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
req.typenames: RM_PROCESS_INFO, *PRM_PROCESS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_PROCESS_INFO
 - restartmanager/_RM_PROCESS_INFO
 - PRM_PROCESS_INFO
 - restartmanager/PRM_PROCESS_INFO
 - RM_PROCESS_INFO
 - restartmanager/RM_PROCESS_INFO
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
 - RM_PROCESS_INFO
---

# RM_PROCESS_INFO structure


## -description

Describes an application that is to be registered with the Restart Manager.

## -struct-fields

### -field Process

Contains an <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a> structure that  uniquely identifies the application by its PID and the time the process began.

### -field strAppName

If the process is a service, this parameter returns the long name for the service. If the process is not a service, this parameter returns the  user-friendly name for the application. If the process is a critical process, and the installer is run  with elevated privileges, this parameter returns the name of the executable file of the critical process. If the process is a critical process, and the installer is run as a service, this parameter returns the long name of the critical process.

### -field strServiceShortName

If the process is a service,  this is the short name for the service. This member is not used if the process is not a service.

### -field ApplicationType

Contains an <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_app_type">RM_APP_TYPE</a> enumeration value that specifies the type of application as <b>RmUnknownApp</b>,  <b>RmMainWindow</b>, <b>RmOtherWindow</b>, <b>RmService</b>, <b>RmExplorer</b> or <b>RmCritical</b>.

### -field AppStatus

Contains a bit mask that describes the current status of the application. See the <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_app_status">RM_APP_STATUS</a> enumeration.

### -field TSSessionId

Contains the Terminal Services session ID 
							of the process.  If the terminal session of the process cannot be determined, the value of this member is set to <b>RM_INVALID_SESSION</b> (-1).
This member is not used if the process is a service  or a  system critical process.

### -field bRestartable

<b>TRUE</b> if the application can be restarted by the Restart Manager; otherwise, <b>FALSE</b>.
This member is always <b>TRUE</b> if the process is a service. This member is always  <b>FALSE</b> if the process is a critical system process.

## -see-also

<a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_app_type">RM_APP_TYPE</a>



<a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_filter_info">RM_FILTER_INFO</a>



<a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetlist">RmGetList</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a>