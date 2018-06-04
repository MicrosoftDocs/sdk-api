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

# DavUnregisterAuthCallback function


## -description


Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.


## -parameters




### -param hCallback [in]

The opaque handle that was returned by the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.


## -returns



This function does not return a value.




## -remarks



To register the callback function, use the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a>
 

 

