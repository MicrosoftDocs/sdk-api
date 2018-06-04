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

# HANDLE_CREATION_OPTIONS enumeration


## -description


Represents the action to take on a file that exists or doesn't exist. 


## -enum-fields




### -field HCO_CREATE_NEW

Create a new file, only if it doesn't already exist.



### -field HCO_CREATE_ALWAYS

Create a new file, always.



### -field HCO_OPEN_EXISTING

Open a file only if it exists.


### -field HCO_OPEN_ALWAYS

Open a file, always.


### -field HCO_TRUNCATE_EXISTING

Open a file and truncates it so that its size is zero bytes, only if it exists.


