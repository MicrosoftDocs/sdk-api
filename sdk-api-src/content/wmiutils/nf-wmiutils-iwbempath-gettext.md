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

# IWbemPath::GetText


## -description


The 
<b>IWbemPath::GetText</b> method returns a textual representation of a path that has previously been placed into a parser object.


## -parameters




### -param lFlags [in]

Flag which controls how the text is returned.



#### WBEMPATH_COMPRESSED

Obsolete. Do not use.



#### WBEMPATH_GET_RELATIVE_ONLY

Returns the relative path, skips server and namespaces.



#### WBEMPATH_GET_SERVER_TOO

Returns the entire path, including server and namespace.



#### WBEMPATH_GET_SERVER_AND_NAMESPACE_ONLY

Returns only the server and namespace portion of the path. Ignores the class or key portion.



#### WBEMPATH_GET_NAMESPACE_ONLY

Returns only the namespace portion of the path.



#### WBEMPATH_GET_ORIGINAL

Returns whatever was passed in using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> method.


### -param puBuffLength [in, out]

Caller sets this to the size of <i>pszText</i>. If the method is successful, it sets <i>puBufferLength</i> to the number of wide characters used, including the terminating null character.


### -param pszText [in, out]

Textual representation of the path.


## -returns



This method returns the following values.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

