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

# CheckTokenCapability function


## -description


The <b>CheckTokenCapability</b> function checks the capabilities of a given token.


## -parameters




### -param TokenHandle [in, optional]

A handle to an access token. The handle must have TOKEN_QUERY access to the token. The token must be an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>. 
      

If <i>TokenHandle</i> is <b>NULL</b>, <b>CheckTokenCapability</b> uses the impersonation token of the calling thread. If the thread is not impersonating, the function duplicates the thread's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> to create an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


### -param CapabilitySidToCheck [in]

A pointer to a capability <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure. The <b>CheckTokenCapability</b> function checks the capabilities of this access token.


### -param HasCapability [out]

Receives the results of the check. If the access token has the capability, it returns <b>TRUE</b>, otherwise, it returns <b>FALSE</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>




