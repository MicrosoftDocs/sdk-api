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

# DavRegisterAuthCallback function


## -description


Registers an application-defined callback function that the WebDAV client can use to prompt the user for credentials.


## -parameters




### -param CallBack [in]

A pointer to a function of type <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">PFNDAVAUTHCALLBACK</a>.


### -param Version [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is an opaque handle. Note that <b>OPAQUE_HANDLE</b> is defined to be a <b>DWORD</b> value.




## -remarks



The WebDAV client uses the callback function when it is unable to connect to a remote resource using default credentials.

To unregister the callback function, use the <a href="https://msdn.microsoft.com/5277d9ce-22e6-49d5-9a9c-c02993605bdf">DavUnregisterAuthCallback</a> function, passing the returned opaque handle in the <i>hCallback</i>  parameter.




## -see-also




<a href="https://msdn.microsoft.com/5277d9ce-22e6-49d5-9a9c-c02993605bdf">DavUnregisterAuthCallback</a>
 

 

