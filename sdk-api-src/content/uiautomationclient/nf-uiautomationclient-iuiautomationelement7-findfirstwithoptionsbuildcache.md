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

# IUIAutomationElement7::FindFirstWithOptionsBuildCache


## -description


Finds the first matching element in the specified order, but also caches its properties and pattern.


## -parameters




### -param scope [in]

A combination of values specifying the scope of the search.


### -param condition [in]

A pointer to a condition that represents the criteria to match.


### -param cacheRequest [in]

A pointer to a cache request that specifies the control patterns and properties to include in the cache.


### -param traversalOptions

Enumeration value specifying the tree navigation order.


### -param root [in, optional]

A pointer to the element with which to begin the search.


### -param found






#### - foundElement [out, retval]

Receives a pointer to the element. <b>NULL</b> is returned if no matching element is found.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62B3D170-C3B3-48B8-92F8-3DF02F5D4082">IUIAutomationElement7</a>
 

 

