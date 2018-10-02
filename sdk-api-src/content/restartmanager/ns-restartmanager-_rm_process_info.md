---
UID: NS:restartmanager._RM_PROCESS_INFO
title: "_RM_PROCESS_INFO"
author: windows-sdk-content
description: Describes an application that is to be registered with the Restart Manager.
old-location: rstmgr\rm_process_info.htm
tech.root: RstMgr
ms.assetid: 27e593f9-8ff0-4de4-87ca-7fa5f324468a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PRM_PROCESS_INFO, RM_PROCESS_INFO, RM_PROCESS_INFO structure [Restart Mgr], _RM_PROCESS_INFO, restartmanager/_RM_PROCESS_INFO, rstmgr.rm_process_info"
ms.prod: windows
ms.technology: windows-sdk
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
 - RM_PROCESS_INFO
product: Windows
targetos: Windows
req.typenames: RM_PROCESS_INFO, *PRM_PROCESS_INFO
req.redist: 
---

# _RM_PROCESS_INFO structure


## -description


Describes an application that is to be registered with the Restart Manager.


## -struct-fields




### -field Process

Contains an <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure that  uniquely identifies the application by its PID and the time the process began.


### -field strAppName

If the process is a service, this parameter returns the long name for the service. If the process is not a service, this parameter returns the  user-friendly name for the application. If the process is a critical process, and the installer is run  with elevated privileges, this parameter returns the name of the executable file of the critical process. If the process is a critical process, and the installer is run as a service, this parameter returns the long name of the critical process.  



### -field strServiceShortName

If the process is a service,  this is the short name for the service. This member is not used if the process is not a service.


### -field ApplicationType

Contains an <a href="https://msdn.microsoft.com/f980b11c-8de1-45dc-b514-8f4cf571afa6">RM_APP_TYPE</a> enumeration value that specifies the type of application as <b>RmUnknownApp</b>,  <b>RmMainWindow</b>, <b>RmOtherWindow</b>, <b>RmService</b>, <b>RmExplorer</b> or <b>RmCritical</b>.


### -field AppStatus

Contains a bit mask that describes the current status of the application. See the <a href="https://msdn.microsoft.com/cb3fe44b-1049-4189-a19a-b5a8fec6daf8">RM_APP_STATUS</a> enumeration.


### -field TSSessionId

Contains the Terminal Services session ID 
							of the process.  If the terminal session of the process cannot be determined, the value of this member is set to <b>RM_INVALID_SESSION</b> (-1).
This member is not used if the process is a service  or a  system critical process.


### -field bRestartable

<b>TRUE</b> if the application can be restarted by the Restart Manager; otherwise, <b>FALSE</b>.
This member is always <b>TRUE</b> if the process is a service. This member is always  <b>FALSE</b> if the process is a critical system process.


## -see-also




<a href="https://msdn.microsoft.com/f980b11c-8de1-45dc-b514-8f4cf571afa6">RM_APP_TYPE</a>



<a href="https://msdn.microsoft.com/b0fd12e4-20e3-48d1-a2db-c1e0334ed427">RM_FILTER_INFO</a>



<a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a>



<a href="https://msdn.microsoft.com/de4feea4-2b45-4430-a4b3-8ca26c455e42">RmGetList</a>



<a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a>



<a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a>
 

 

