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

# WICComponentEnumerateOptions enumeration


## -description


Specifies component enumeration options.


## -enum-fields




### -field WICComponentEnumerateDefault

Enumerate any components that are not disabled. Because this value is 0x0, it is always included with the other options.


### -field WICComponentEnumerateRefresh

Force a read of the registry before enumerating components.


### -field WICComponentEnumerateDisabled

Include disabled components in the enumeration. The set of disabled components is disjoint with the set of default enumerated components


### -field WICComponentEnumerateUnsigned

Include unsigned components in the enumeration. This option has no effect.


### -field WICComponentEnumerateBuiltInOnly

At the end of component enumeration, filter out any components that are not Windows provided.


### -field WICCOMPONENTENUMERATEOPTIONS_FORCE_DWORD



