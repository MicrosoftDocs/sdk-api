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

# HANDLE_ACCESS_OPTIONS enumeration


## -description


Defines the level of access that a handle has on files. 


## -enum-fields




### -field HAO_NONE

None.


### -field HAO_READ_ATTRIBUTES

The handle can be used to read file attributes.


### -field HAO_READ

The handle can be used to read the file.


### -field HAO_WRITE

The handle can be used to write to the file.


### -field HAO_DELETE

The handle can be used to delete the file.

