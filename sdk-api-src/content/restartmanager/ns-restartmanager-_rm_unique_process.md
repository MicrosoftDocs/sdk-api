---
UID: NS:restartmanager._RM_UNIQUE_PROCESS
title: "_RM_UNIQUE_PROCESS"
author: windows-driver-content
description: Uniquely identifies a process by its PID and the time the process began.
old-location: rstmgr\rm_unique_process.htm
old-project: RstMgr
ms.assetid: 5e3698c7-1ea8-4f9d-8fae-e69055a000fc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PRM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS structure [Restart Mgr], RM_UNIQUE_PROCESS, RM_UNIQUE_PROCESS structure [Restart Mgr], _RM_UNIQUE_PROCESS, restartmanager/*PRM_UNIQUE_PROCESS, restartmanager/_RM_UNIQUE_PROCESS, rstmgr.rm_unique_process"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	RestartManager.h
api_name:
-	RM_UNIQUE_PROCESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _RM_UNIQUE_PROCESS structure


## -description


Uniquely identifies a process by its PID and the time the process began.  An array of <b>RM_UNIQUE_PROCESS</b> structures can be passed to  the <a href="https://msdn.microsoft.com/9ac94461-bf75-4517-b47e-23d82474efe8">RmRegisterResources</a> function. 


## -struct-fields




### -field dwProcessId

The product identifier (PID).


### -field ProcessStartTime

The creation time of the process. The time is provided as a <b>FILETIME</b> structure that is returned by the <i>lpCreationTime</i> parameter of the <a href="https://msdn.microsoft.com/4c1e8bd4-5ed2-4c97-bc4f-1083a8b24623">GetProcessTimes</a> function. 


## -remarks



The <b>RM_UNIQUE_PROCESS</b> structure can be used to uniquely identify an application in an <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structure or  registered with the Restart Manager session by the <a href="https://msdn.microsoft.com/9ac94461-bf75-4517-b47e-23d82474efe8">RmRegisterResources</a> function.



