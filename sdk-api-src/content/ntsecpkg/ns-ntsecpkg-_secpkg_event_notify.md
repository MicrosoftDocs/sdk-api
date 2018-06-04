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

# _SECPKG_EVENT_NOTIFY structure


## -description


The <b>SECPKG_EVENT_NOTIFY</b> structure contains information about security events. This structure is passed to a function registered to receive event notifications. Event notification functions are registered by calling the 
<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> function.


## -struct-fields




### -field EventClass

The event class.


### -field Reserved

Reserved.


### -field EventDataSize

The size of the <b>EventData</b> member.


### -field EventData

The event details.


### -field PackageParameter

Information specified as the <i>Parameter</i> value when <a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> is called to register for notification.

