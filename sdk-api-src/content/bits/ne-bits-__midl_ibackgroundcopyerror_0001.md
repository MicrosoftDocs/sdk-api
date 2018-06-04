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

# __MIDL_IBackgroundCopyError_0001 enumeration


## -description


The 
<b>BG_ERROR_CONTEXT</b> enumeration defines the constant values that specify the context in which the error occurred.


## -enum-fields




### -field BG_ERROR_CONTEXT_NONE

An error has not occurred.


### -field BG_ERROR_CONTEXT_UNKNOWN

The error context is unknown.


### -field BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER

The transfer queue manager generated the error.


### -field BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION

The error was generated while the queue manager was notifying the client of an event.


### -field BG_ERROR_CONTEXT_LOCAL_FILE

The error was related to the specified local file. For example, permission was denied or the volume was unavailable.


### -field BG_ERROR_CONTEXT_REMOTE_FILE

The error was related to the specified remote file. For example, the URL was not accessible.


### -field BG_ERROR_CONTEXT_GENERAL_TRANSPORT

The transport layer generated the error. These errors are general transport failures  (these errors  are not specific to the remote file).


### -field BG_ERROR_CONTEXT_REMOTE_APPLICATION

The server application that BITS passed the upload file to generated an error while processing the upload file. 

<b>BITS 1.2 and earlier:  </b>Not supported.


## -see-also




<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">IBackgroundCopyError::GetError</a>



<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">IBackgroundCopyError::GetErrorContextDescription</a>
 

 

