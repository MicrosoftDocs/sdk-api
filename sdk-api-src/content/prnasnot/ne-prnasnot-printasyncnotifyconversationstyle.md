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

# PrintAsyncNotifyConversationStyle enumeration


## -description


Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.


## -enum-fields




### -field kBiDirectional

Indicates that applications can send replies to the Print Spooler-hosted component that sent a notification.


### -field kUniDirectional

Indicates that communication goes only from the Print Spooler-hosted component to one or more listening applications.


## -remarks



Even when the communication is bidirectional, applications cannot initiate communication. They can only reply to notifications sent by the Print Spooler-hosted components.

When multiple applications listen for bidirectional notifications, they receive only the first notification sent through a bidirectional channel. The Print Spooler maintains the channel only with the first listening application that responded, and discards all subsequent replies from other listeners.



