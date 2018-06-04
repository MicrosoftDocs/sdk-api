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

# PDOPSTATUS enumeration


## -description


Provides operation status flags.


## -enum-fields




### -field PDOPS_RUNNING

Operation is running, no user intervention.


### -field PDOPS_PAUSED

Operation has been paused by the user.


### -field PDOPS_CANCELLED

Operation has been canceled by the user - now go undo.


### -field PDOPS_STOPPED

Operation has been stopped by the user - terminate completely.


### -field PDOPS_ERRORS

Operation has gone as far as it can go without throwing error dialogs.

