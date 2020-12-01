---
UID: NS:restartmanager._RM_UNIQUE_PROCESS
title: RM_UNIQUE_PROCESS (restartmanager.h)
description: Uniquely identifies a process by its PID and the time the process began.
helpviewer_keywords: ["*PRM_UNIQUE_PROCESS","*PRM_UNIQUE_PROCESS structure [Restart Mgr]","RM_UNIQUE_PROCESS","RM_UNIQUE_PROCESS structure [Restart Mgr]","restartmanager/*PRM_UNIQUE_PROCESS","restartmanager/_RM_UNIQUE_PROCESS","rstmgr.rm_unique_process"]
old-location: rstmgr\rm_unique_process.htm
tech.root: rstmgr
ms.assetid: 5e3698c7-1ea8-4f9d-8fae-e69055a000fc
ms.date: 12/05/2018
ms.keywords: '*PRM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS structure [Restart Mgr], RM_UNIQUE_PROCESS, RM_UNIQUE_PROCESS structure [Restart Mgr], restartmanager/*PRM_UNIQUE_PROCESS, restartmanager/_RM_UNIQUE_PROCESS, rstmgr.rm_unique_process'
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
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_UNIQUE_PROCESS
 - restartmanager/_RM_UNIQUE_PROCESS
 - PRM_UNIQUE_PROCESS
 - restartmanager/PRM_UNIQUE_PROCESS
 - RM_UNIQUE_PROCESS
 - restartmanager/RM_UNIQUE_PROCESS
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
 - RM_UNIQUE_PROCESS
---

# RM_UNIQUE_PROCESS structure


## -description

Uniquely identifies a process by its PID and the time the process began.  An array of <b>RM_UNIQUE_PROCESS</b> structures can be passed to  the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmregisterresources">RmRegisterResources</a> function.

## -struct-fields

### -field dwProcessId

The product identifier (PID).

### -field ProcessStartTime

The creation time of the process. The time is provided as a <b>FILETIME</b> structure that is returned by the <i>lpCreationTime</i> parameter of the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesstimes">GetProcessTimes</a> function.

## -remarks

The <b>RM_UNIQUE_PROCESS</b> structure can be used to uniquely identify an application in an <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structure or  registered with the Restart Manager session by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmregisterresources">RmRegisterResources</a> function.