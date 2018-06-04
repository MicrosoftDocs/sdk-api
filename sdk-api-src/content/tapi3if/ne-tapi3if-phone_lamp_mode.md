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

# PHONE_LAMP_MODE enumeration


## -description


The 
<b>PHONE_LAMP_MODE</b> enum provides indicators of a phone lamp's status.


## -enum-fields




### -field LM_DUMMY

The lamp identifier has no corresponding lamp.


### -field LM_OFF

The lamp is off.


### -field LM_STEADY

The lamp is on steadily.


### -field LM_WINK

The lamp is winking, which means on and off at a normal rate.


### -field LM_FLASH

The lamp is flashing, which means a slow on and off.


### -field LM_FLUTTER

The lamp is fluttering, which means a fast on and off.


### -field LM_BROKENFLUTTER

The lamp is flashing, which means superposition of a flash and flutter.


### -field LM_UNKNOWN

The lamp mode is not known.


## -see-also




<a href="https://msdn.microsoft.com/5e0fa135-304a-4598-a6cd-2e5734b3678c">ITPhone::get_LampMode</a>



<a href="https://msdn.microsoft.com/0445cf2c-1b00-4136-bdab-3c6e0669ef11">ITPhone::put_LampMode</a>
 

 

