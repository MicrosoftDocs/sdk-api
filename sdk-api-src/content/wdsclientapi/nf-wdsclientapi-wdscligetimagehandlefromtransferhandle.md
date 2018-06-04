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

# WdsCliGetImageHandleFromTransferHandle function


## -description


Returns an image handle from a completed transfer handle.  The handle is to the local copy of the image that's been transferred from the server to the client.


## -parameters




### -param hTransfer

A WDS transfer handle that has completed the transfer. This can be the handle returned by the <a href="https://msdn.microsoft.com/43590cee-20d5-47da-8e35-fa4fda1da175">WdsCliTransferImage</a> or <a href="https://msdn.microsoft.com/d219b7ee-4cb8-43ce-959b-4793c7df17ff">WdsCliTransferFile</a> functions.


### -param phImageHandle [out]

A pointer to a location that contains an image handle.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



If the transfer is not yet complete when this function is called, it will return an error code.

Use the <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function to close the image handle returned by this function.



