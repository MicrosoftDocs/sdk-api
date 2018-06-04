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

# LIBRARYMANAGEDIALOGOPTIONS enumeration


## -description


Used by <a href="https://msdn.microsoft.com/1ac911bb-28d6-4cb6-a66a-1a0c8a4bd6a1">SHShowManageLibraryUI</a> to define options for handling a name collision when saving a library.


## -enum-fields




### -field LMD_DEFAULT

Show default warning UI to the user.


### -field LMD_ALLOWUNINDEXABLENETWORKLOCATIONS

Do not display a warning dialog to the user in collisions that concern network locations that cannot be indexed.

