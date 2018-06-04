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

# MSPEVENTITEM structure


## -description


The 
<b>MSPEVENTITEM</b> structure contains link pointers and event types for MSP events.


## -struct-fields




### -field Link

Doubly-linked list. Part of Windows 2000 run-time routines that are callable by both kernel mode code in the executive and user mode code in various subsystems. See Ntrtl.h or search the Platform SDK for details.


### -field MSPEventInfo

The 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> structure contains information concerning an event.

