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

# WSManCloseOperation function


## -description


Cancels or closes an asynchronous operation. All resources that are associated with the operation are freed.


## -parameters




### -param operationHandle [in, out, optional]

Specifies the operation handle to be closed.


### -param flags

Reserved for future use. Set to zero.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




## -remarks



The method de-allocates local and remote resources associated with the operation. After the <b>WSManCloseOperation</b> method is called, the <i>operationHandle</i> parameter cannot be passed to any other call. If the callback associated with the operation is pending and has not completed before <b>WSManCloseOperation</b> is called, the operation is marked for deletion and the method returns immediately.



