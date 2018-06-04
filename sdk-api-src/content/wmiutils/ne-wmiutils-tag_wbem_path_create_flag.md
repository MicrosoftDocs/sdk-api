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

# tag_WBEM_PATH_CREATE_FLAG enumeration


## -description


Contains flags specifying the type of paths accepted.


## -enum-fields




### -field WBEMPATH_CREATE_ACCEPT_RELATIVE

Allow paths without server names.


### -field WBEMPATH_CREATE_ACCEPT_ABSOLUTE

Reserved for future use.


### -field WBEMPATH_CREATE_ACCEPT_ALL

Allow setting an empty path (which additionally clears out the object), Also allows paths which have just the server names, or paths which don't have server names.


### -field WBEMPATH_TREAT_SINGLE_IDENT_AS_NS

A simple path, such as "XYZ" is interpreted as a namespace.

