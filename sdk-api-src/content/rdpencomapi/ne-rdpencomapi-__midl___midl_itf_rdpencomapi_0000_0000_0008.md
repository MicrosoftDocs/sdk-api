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

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0008 enumeration


## -description


Defines values for the type of  application.  You can retrieve these flags  from the <a href="https://msdn.microsoft.com/9a934718-1eea-4406-a1da-b7d493f6667e">IRDPSRAPIApplication</a> interface that represents each application.

You can retrieve the list of applications that are running on the sharing user session  for both the sharer and the viewer through the <a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a> interface by calling the <a href="https://msdn.microsoft.com/08704192-320d-44f2-a811-f8565285bd30">get_Applications</a> method.


## -enum-fields




### -field APP_FLAG_PRIVILEGED

This flag indicates that the application cannot be shared. The application runs at a higher level than the process that is using the Windows Desktop Sharing API. An application can use this flag to prevent the user from sharing it by either disabling the entry for the application in the user interface or by not showing the entry.

