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

# tag_WBEM_GET_TEXT_FLAGS enumeration


## -description


Contains flags which controls how the text is returned.


## -enum-fields




### -field WBEMPATH_COMPRESSED

Obsolete. Do not use.


### -field WBEMPATH_GET_RELATIVE_ONLY

Returns the relative path, skips server and namespaces.


### -field WBEMPATH_GET_SERVER_TOO

Returns the entire path, including server and namespace.


### -field WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY

Returns only the server and namespace portion of the path. Ignores the class or key portion.


### -field WBEMPATH_GET_NAMESPACE_ONLY

Returns only the namespace portion of the path.


### -field WBEMPATH_GET_ORIGINAL

Returns whatever was passed in using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> method.

