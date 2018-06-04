---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _RM_APP_TYPE enumeration


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
 

 

