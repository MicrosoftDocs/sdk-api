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

# _SecPkgContext_ClientCreds structure


## -description


The <b>SecPkgContext_ClientCreds</b> structure specifies client credentials when calling the <a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a> function.

This structure is supported only on the server.


## -struct-fields




### -field AuthBufferLen

The size, in characters, of the <b>AuthBuffer</b> buffer.


### -field AuthBuffer

A pointer to a buffer that represents the client credentials.


## -see-also




<a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a>
 

 

