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

# HANDLE_SHARING_OPTIONS enumeration


## -description


Defines the requested sharing mode of the file handle.


## -enum-fields




### -field HSO_SHARE_NONE

Prevents other processes from opening a file if they request delete, read, or write access.


### -field HSO_SHARE_READ

Enables subsequent open operations on a file to request read access.
Otherwise, other processes cannot open the file if they request read access.




### -field HSO_SHARE_WRITE

Enables subsequent open operations on a file to request write access.
Otherwise, other processes cannot open the file if they request write access.



### -field HSO_SHARE_DELETE

Enables subsequent open operations on a file to request delete access.
Otherwise, other processes cannot open the file if they request delete access.


