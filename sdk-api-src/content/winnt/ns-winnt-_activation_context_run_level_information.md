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

# _ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION structure


## -description


The <b>ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION</b> structure is used by the <a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function.


## -struct-fields




### -field ulFlags

This parameter is reserved for future use. This parameter currently returns 0.


### -field RunLevel

A  <a href="https://msdn.microsoft.com/3bf75a4d-a209-43e4-9fe2-f7da1602fc6c">ACTCTX_REQUESTED_RUN_LEVEL</a> enumeration value that gives the requested run level of the activation context. 


### -field UiAccess

This parameter returns zero if the <b>uiAccess</b> attribute in the application manifest is false. This parameter returns a non-zero value if the <b>uiAccess</b> attribute in the manifest is true. True means that UI accessibility applications require access higher privileges.

