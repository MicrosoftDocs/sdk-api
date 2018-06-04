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

# SHChangeNotification_Unlock function


## -description


Unlocks shared memory for a change notification.


## -parameters




### -param hLock [in]

Type: <b>HANDLE</b>

A handle to the memory lock. This is the handle returned by <a href="https://msdn.microsoft.com/8e22d5d0-64be-403c-982d-c23705d85223">SHChangeNotification_Lock</a> when it locked the memory.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> on success; otherwise, <b>FALSE</b>.



