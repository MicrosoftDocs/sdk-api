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

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0007 enumeration


## -description


Defines values for the type of window. These flags can be retrieved from the <a href="https://msdn.microsoft.com/85c8263b-e796-4748-b8e5-6315e5937861">IRDPSRAPIWindow</a> interface that represents each Win32 window.

The list of windows on the sharing user session can be retrieved on both the sharer and the viewer through the <a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a> interface by calling the <a href="https://msdn.microsoft.com/cc964964-0f3a-410c-b1f4-426abd9c1a22">get_Windows</a> method.


## -enum-fields




### -field WND_FLAG_PRIVILEGED

The window is part of an application that runs at a higher level than the current process. This flag indicates that the window cannot be shared. Applications can use this flag to prevent the user from sharing it either by disabling the entry for the window in the user interface or by not showing the entry.


## -see-also




<a href="https://msdn.microsoft.com/ceda755a-dd9a-4d89-96b2-39e2dca46801">Windows Desktop Sharing Enumerations</a>
 

 

