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

# MBN_MSG_STATUS enumeration


## -description


The <b>MBN_MSG_STATUS</b> enumerated type defines the type of message being handled.


## -enum-fields




### -field MBN_MSG_STATUS_NEW

The received message is newly arrived or unread.


### -field MBN_MSG_STATUS_OLD

The received message is old and read.


### -field MBN_MSG_STATUS_DRAFT

The outgoing message is unsent and stored in the device.


### -field MBN_MSG_STATUS_SENT

The outgoing message is already sent.

