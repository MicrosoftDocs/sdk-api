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

# ClusterGroupSetEnum function


## -description


Returns the next enumerable object.


## -parameters




### -param hGroupSetEnum [in]

A handle to an open cluster node enumeration
    returned by <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



### -param dwIndex [in]

The index to enumerate, zero for the first call to this function and then
    incremented for subsequent calls.


### -param lpszName [out]

Points to a buffer that receives the name of the object,
    including the terminating null character.


### -param lpcchName [in, out]

Points to a variable that specifies the size, in characters,
    of the buffer pointed to by the <i>lpszName</i> parameter. This size
    should include the terminating null character. When the function
    returns, the variable contains the
    number of characters stored in the buffer, not including the terminating null character.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



