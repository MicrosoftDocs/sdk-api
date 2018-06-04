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

# IWbemPath::GetServer


## -description


The 
<b>IWbemPath::GetServer</b> method retrieves the server portion of the path.


## -parameters




### -param puNameBufLength [in, out]

Upon input, this is the size in characters of the buffer pointed to by <i>pszName</i>. Upon return, this is the number of characters in the server name, including the <b>NULL</b> terminator.


### -param pName






#### - pszName [in, out]

Server name.


## -returns



This method returns the following values.




## -remarks



This method can be used to determine how big a buffer is needed for <i>pszName</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puNameBufLength</i> to 0 (zero) and then making the call. Upon return, <i>puNameBufLength</i> indicates how large a buffer is needed for <i>pszName</i> and its terminating <b>NULL</b> character.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

