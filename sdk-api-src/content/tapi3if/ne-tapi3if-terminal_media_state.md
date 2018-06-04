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

# TERMINAL_MEDIA_STATE enumeration


## -description


The 
<b>TERMINAL_MEDIA_STATE</b> enum indicates the state of a file terminal.


## -enum-fields




### -field TMS_IDLE

The file terminal is idle.


### -field TMS_ACTIVE

The file terminal is active.


### -field TMS_PAUSED

The file terminal is paused.


### -field TMS_LASTITEM

Last item in this enum.


## -see-also




<a href="https://msdn.microsoft.com/f75537e8-f54c-4165-ba89-013eeabceb74">ITFileTerminalEvent::get_State</a>



<a href="https://msdn.microsoft.com/d28063cc-12fe-45b1-8f6a-8c2436926e12">ITMediaControl::get_MediaState</a>
 

 

