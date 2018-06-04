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

# _WLX_NOTIFICATION_INFO structure


## -description


<p class="CCE_Message">[The WLX_NOTIFICATION_INFO structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

This structure stores information about a <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> event.


## -struct-fields




### -field Size

Indicates the size of the structure, in bytes. Your application can check this value against the structure size to validate the structure.


### -field Flags

Reserved for internal use.


### -field UserName

String that specifies the name of the user currently logged on to the system. If the event occurs before a user logs on, this value is <b>NULL</b>.


### -field Domain

String that specifies the name of the domain the user is currently logged on to. If the event occurs before a user logs on, this value is <b>NULL</b>.


### -field WindowStation

Specifies the name of the window station the user is currently logged on to. If the event occurs before a user logs on, this value is <b>NULL</b>. Note that most configurations use a single, default window station. Some applications, such as 
<a href="https://msdn.microsoft.com/5b5b0f97-f973-4f52-a965-c9c2390e6c8d">About Terminal Services</a>, use multiple window stations.


### -field hToken

A handle to the user's token. This value is <b>NULL</b> if the event occurs before a user logs on.


### -field hDesktop

A handle to the desktop that is currently active.


### -field pStatusCallback

Reserved for internal use.

