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

# IWbemPath::GetScope


## -description


The 
<b>IWbemPath::GetScope</b> method retrieves a scope based upon an index. This method retrieves the class name and a 
<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a> pointer so that the details of the keys can be retrieved.


## -parameters




### -param uIndex [in]

Index of the scope.


### -param puClassNameBufSize [in, out]

Caller sets this to the number of characters that the buffer can hold. Upon success, this is set to the number of characters copied into the buffer including the <b>NULL</b> terminator.


### -param pszClass [out]

Buffer where the scope is to be copied.


### -param pKeyList [out]

Pointer to an 
<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a> object.


## -returns



This method returns the following values.




## -remarks



This method can be used to determine how big a buffer is needed for <i>pszClass</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puClassNameBufSize</i> to 0 and then making the call. Upon return, <i>puClassNameBufSize</i> indicates how large of a buffer is needed for <i>pszClass</i> and its terminating <b>NULL</b> character.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 

