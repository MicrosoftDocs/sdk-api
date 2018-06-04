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

# WICProgressNotification enumeration


## -description


Specifies when the progress notification callback should be called.


## -enum-fields




### -field WICProgressNotificationBegin

The callback should be called when codec operations begin.


### -field WICProgressNotificationEnd

The callback should be called when codec operations end.


### -field WICProgressNotificationFrequent

The callback should be called frequently to report status.


### -field WICProgressNotificationAll

The callback should be called on all available progress notifications.


### -field WICPROGRESSNOTIFICATION_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>
 

 

