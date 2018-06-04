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

# FindSyncContextFromName function


## -description


Retrieves the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the specified user name.


## -parameters




### -param pNameCache [in]

A pointer to the name cache that the client is to use.


### -param lpbName [in]

A pointer to the name of the cached item.


### -param cbName [in]

The size, in bytes, of the value in <i>lpbName</i>.


### -param pfnCallback [in]

A pointer to a <a href="https://msdn.microsoft.com/9fcdbca6-95db-4ec1-b81c-3681e9e2bffb">FCACHE_READ_CALLBACK</a> function.

<div class="alert"><b>Note</b>  If this parameter is <b>NULL</b>, no callback function is called.</div>
<div> </div>

### -param lpvClientContext [in]

A pointer to the context that is associated with the client. This context is passed to the callback function.


### -param hToken [in]

Request the cache to evaluate the embedded security descriptor. If <i>hToken</i> is zero, it is ignored.


### -param accessMask [in]

The security descriptor data. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>.


### -param ppContext [out]

A pointer to a pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the user name.

If the function returns <b>TRUE</b>, this parameter can return a <b>NULL</b> pointer. This occurs when the user passes a <b>NULL</b> FIO_CONTEXT to <a href="https://msdn.microsoft.com/4f4bbfda-3be0-41d3-9087-d46edd2e21a3">_AssociateContextWithName</a>.


## -returns



Returns <b>TRUE</b> if the name is found in the cache; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/4f4bbfda-3be0-41d3-9087-d46edd2e21a3">AssociateContextWithName</a>



<a href="https://msdn.microsoft.com/9fcdbca6-95db-4ec1-b81c-3681e9e2bffb">FCACHE_READ_CALLBACK</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

