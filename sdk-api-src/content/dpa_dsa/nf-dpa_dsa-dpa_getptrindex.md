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

# DPA_GetPtrIndex function


## -description


<p class="CCE_Message">[<b>DPA_GetPtrIndex</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Gets the index of a matching item found in a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

Type: <b>HDPA</b>

A handle to an existing DPA.


### -param p

TBD




#### - pvoid [in]

Type: <b>const void*</b>

A pointer to an item to locate in <i>hdpa</i>.


## -returns



Type: <b>int</b>

The index of the item pointed to by <i>pvoid</i>, if found; otherwise, -1.




## -remarks



<b>DPA_GetPtrIndex</b> is not exported by name. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 333 from ComCtl32.dll to obtain a function pointer.



