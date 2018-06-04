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

# FWPM_NET_EVENT_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_NET_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a network event.


## -struct-fields




### -field enumTemplate

Address of an <a href="https://msdn.microsoft.com/79711b24-e092-4a36-810a-6acad279eb90">FWPM_NET_EVENT_ENUM_TEMPLATE0</a> structure. Notifications are only dispatched for objects that match the template. If
   <b>enumTemplate</b> is <b>NULL</b>, it matches all objects.


### -field flags

Unused.


### -field sessionKey

Identifies the session which created the subscription.


## -remarks



<b>FWPM_NET_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_NET_EVENT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



