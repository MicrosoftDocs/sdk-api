---
UID: NE:restartmanager._RM_APP_TYPE
title: RM_APP_TYPE
author: windows-sdk-content
description: Specifies the type of application that is described by the RM_PROCESS_INFO structure.
old-location: rstmgr\rm_app_type.htm
tech.root: rstmgr
ms.assetid: f980b11c-8de1-45dc-b514-8f4cf571afa6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RM_APP_TYPE, RmConsole, RmCritical, RmExplorer, RmMainWindow, RmOtherWindow, RmService, RmUnknownApp, _RM_APP_TYPE, _RM_APP_TYPE enumeration [Restart Mgr], restartmanager/RmConsole, restartmanager/RmCritical, restartmanager/RmExplorer, restartmanager/RmMainWindow, restartmanager/RmOtherWindow, restartmanager/RmService, restartmanager/RmUnknownApp, restartmanager/_RM_APP_TYPE, rstmgr.rm_app_type
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RM_APP_TYPE
product: Windows
targetos: Windows
req.typenames: RM_APP_TYPE
req.redist: 
---

# RM_APP_TYPE enumeration


## -description


Specifies the type of application that is described by the <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structure.


## -enum-fields




### -field RmUnknownApp

The application cannot be classified as any other type. An application of this type can only be shut down by a forced shutdown.


### -field RmMainWindow

A Windows application run as a stand-alone process that displays a top-level window.


### -field RmOtherWindow

A Windows application that does not run as a stand-alone process and does not display a top-level window.


### -field RmService

The application is a Windows service.


### -field RmExplorer

The application is Windows Explorer.


### -field RmConsole

The application is a stand-alone console application.


### -field RmCritical

A system restart is required to complete the installation because a process cannot be shut down. The process cannot be shut down because of the following reasons.  The process may be a critical process.  The current user may not have permission to shut down the process. The process may belong to the primary installer that started the Restart Manager. 


## -see-also




<a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a>
 

 

