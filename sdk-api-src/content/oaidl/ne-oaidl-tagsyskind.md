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

# tagSYSKIND enumeration


## -description


Identifies the target operating system platform.


## -enum-fields




### -field SYS_WIN16

The target operating system for the type library is 16-bit Windows. By default, data members are packed.



### -field SYS_WIN32

The target operating system for the type library is 32-bit Windows. By default, data members are naturally aligned (for example, 2-byte integers are aligned on even-byte boundaries; 4-byte integers are aligned on quad-word boundaries, and so on).



### -field SYS_MAC

The target operating system for the type library is Apple Macintosh. By default, all data members are aligned on even-byte boundaries.



### -field SYS_WIN64

The target operating system for the type library is 64-bit Windows.

