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

# IWbemPath::SetText


## -description


The 
<b>IWbemPath::SetText</b> method parses a path so that information on the path can be returned by the path parser. Typically, this is the first method called by users of the interface. The only case in which this is not the first method called is when the calling code is constructing the path by specifying each piece separately.


## -parameters




### -param uMode [in]

Flag specifying the type of paths accepted.



#### WBEMPATH_CREATE_ACCEPT_RELATIVE

Allow paths without server names.



#### WBEMPATH_CREATE_ACCEPT_ABSOLUTE

Reserved for future use.



#### WBEMPATH_CREATE_ACCEPT_ALL

Allow setting an empty path (which additionally clears out the object), Also allows paths which have just the server names, or paths which don't have server names.



#### WBEMPATH_TREAT_SINGLE_IDENT_AS_NS

A simple path, such as "XYZ" is interpreted as a namespace.


### -param pszPath [in]

Path to be parsed.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

