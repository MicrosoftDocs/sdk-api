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

# SrpEnablePermissiveModeFileEncryption function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Enables permissive mode for file encryption on the current thread and all threads this thread will create or post work to.

Use <a href="https://msdn.microsoft.com/CB75BAFE-EB2A-43F2-8689-34E798C3B9F5">SrpDisablePermissiveModeFileEncryption</a> to disable the mode. 

This API does not attempt to handle nested calls by reference counting or such. Subsequent calls to <b>SrpEnablePermissiveModeFileEncryption</b> after the first successful call to this API will not have any effect.


## -parameters




### -param enterpriseId [in, optional]

Contains enterprise ID string. In TH2 this is not used.


## -returns



If this function succeeds, it returns S_OK. 

HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) indicates that thread tagging cannot be performed due to either process or thread context.



