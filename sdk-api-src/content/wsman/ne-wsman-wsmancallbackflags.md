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

# WSManCallbackFlags enumeration


## -description


Defines a set of flags used by all callback functions.


## -enum-fields




### -field WSMAN_FLAG_CALLBACK_END_OF_OPERATION

Indicates the end of a single step of a multi-step operation. This flag is used for optimization purposes if the shell cannot be determined.


### -field WSMAN_FLAG_CALLBACK_END_OF_STREAM

Indicates the end of a particular stream. This flag is used for optimization purposes if an indication has been provided to the shell that no more output will occur for this stream.


### -field WSMAN_FLAG_CALLBACK_SHELL_SUPPORTS_DISCONNECT


### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTED


### -field WSMAN_FLAG_CALLBACK_NETWORK_FAILURE_DETECTED


### -field WSMAN_FLAG_CALLBACK_RETRYING_AFTER_NETWORK_FAILURE


### -field WSMAN_FLAG_CALLBACK_RECONNECTED_AFTER_NETWORK_FAILURE


### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTING


### -field WSMAN_FLAG_CALLBACK_RETRY_ABORTED_DUE_TO_INTERNAL_ERROR


### -field WSMAN_FLAG_CALLBACK_RECEIVE_DELAY_STREAM_REQUEST_PROCESSED



