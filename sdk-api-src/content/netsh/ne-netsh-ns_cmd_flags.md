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

# NS_CMD_FLAGS enumeration


## -description


The <b>NS_CMD_FLAGS</b> enumeration specifies command flags available in NetShell.


## -enum-fields




### -field CMD_FLAG_PRIVATE

Indicates a private command. This command is not valid in subcontexts.


### -field CMD_FLAG_INTERACTIVE

Indicates an interactive command. This command is not valid from outside NetShell.


### -field CMD_FLAG_LOCAL

Indicates a local command. This command is not valid from remote computers.


### -field CMD_FLAG_ONLINE

Indicates a command is valid only when online. This command is not valid in offline or noncommit mode.


### -field CMD_FLAG_HIDDEN

Indicates a command is not in online Help, but can be executed.


### -field CMD_FLAG_LIMIT_MASK

Indicates that the  command limits the mask.


### -field CMD_FLAG_PRIORITY

Indicates that the <b>ulPriority</b> field is used.

