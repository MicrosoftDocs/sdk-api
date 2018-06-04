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

# _MI_SessionCallbacks structure


## -description


A container for callback function pointers that handle logging and error messages.


## -struct-fields




### -field callbackContext

A client-specific context that is passed to all of the callbacks. This is used to correlate the callback to the associated operation.


#### - writeError

The CIM extension callback for errors. The session version of this function is informative only. The session will fail to create and will  return an error. All parameters are valid only for the lifetime of the callback.


#### - writeMessage

The CIM extension callback for receiving logging from the session creation. All parameters are valid only for the lifetime of the callback.


## -remarks



This is the structure that holds all callback function pointers.  Fill in the ones 
you want to receive.  All callbacks are CIM extensions for tracking
logging and error messages.



