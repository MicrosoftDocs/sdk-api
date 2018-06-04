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

# SHIsLowMemoryMachine function


## -description


Not supported.


## -parameters




### -param dwType [in]

Type: <b>DWORD</b>

The type of machine being examined. The following is the only recognized value.



#### ILMM_IE4

An older (circa 1997), low-end machine. Since system resources in general were lower on these older machines, the low-memory threshold is accordingly lower.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the machine is considered low on resources, <b>FALSE</b> otherwise.

<div class="alert"><b>Note</b>  Always returns <b>FALSE</b> under Windows XP.</div>
<div> </div>


