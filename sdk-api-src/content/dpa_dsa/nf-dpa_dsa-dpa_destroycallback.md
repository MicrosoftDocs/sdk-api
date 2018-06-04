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

# DPA_DestroyCallback function


## -description


<p class="CCE_Message">[<b>DPA_DestroyCallback</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Calls <i>pfnCB</i> on each element of the dynamic pointer array (DPA), then frees the DPA.


## -parameters




### -param hdpa

TBD


### -param pfnCB

Type: <b><a href="https://msdn.microsoft.com/7ee522bc-9a2c-417d-93d7-5f306fba511f">PFNDPAENUMCALLBACK</a></b>

A callback function pointer. See <a href="https://msdn.microsoft.com/7ee522bc-9a2c-417d-93d7-5f306fba511f">PFNDPAENUMCALLBACK</a> for the callback function prototype.


### -param pData

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.


#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



No return value.



