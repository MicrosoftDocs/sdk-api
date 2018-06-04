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

# CALLHUB_STATE enumeration


## -description


The 
<b>CALLHUB_STATE</b> enum is a state indicator returned by the 
<a href="https://msdn.microsoft.com/0ca4bbad-6822-4a8b-8df4-da6e630752f0">ITCallHub::get_State</a> method.


## -enum-fields




### -field CHS_ACTIVE

The CallHub is active. There is at least one call that is not in the CS_DISCONNECTED state.


### -field CHS_IDLE

All calls associated with this CallHub are in the CS_DISCONNECTED state.


## -see-also




<a href="https://msdn.microsoft.com/0ca4bbad-6822-4a8b-8df4-da6e630752f0">ITCallHub::get_State</a>
 

 

