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

# MBN_VOICE_CLASS enumeration


## -description


 The <b>MBN_VOICE_CLASS</b> enumerated type specifies a device's voice capabilities and how they interact with the data service.


## -enum-fields




### -field MBN_VOICE_CLASS_NONE

The device voice class is unknown.


### -field MBN_VOICE_CLASS_NO_VOICE

The device does not support voice calls.


### -field MBN_VOICE_CLASS_SEPARATE_VOICE_DATA

The device supports voice calls, but does not support simultaneous voice and data.


### -field MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA

The device supports simultaneous voice and data.

