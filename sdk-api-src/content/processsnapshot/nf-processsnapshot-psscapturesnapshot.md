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

# PssCaptureSnapshot function


## -description


Captures a snapshot of a target process.


## -parameters




### -param ProcessHandle [in]

A handle to the target process.


### -param CaptureFlags [in]

Flags that specify what to capture. For more information, see <a href="https://msdn.microsoft.com/6146DDA2-2475-45F8-86F3-65791B10743D">PSS_CAPTURE_FLAGS</a>.


### -param ThreadContextFlags [in, optional]

The <b>CONTEXT</b> record flags to capture if <i>CaptureFlags</i> specifies thread contexts.


### -param SnapshotHandle [out]

A handle to the snapshot that this function captures.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.



