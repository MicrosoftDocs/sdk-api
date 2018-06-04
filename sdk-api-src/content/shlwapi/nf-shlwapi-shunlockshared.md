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

# SHUnlockShared function


## -description


<p class="CCE_Message">[<b>SHUnlockShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Unlocks memory locked by <a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>.


## -parameters




### -param pvData [in]

Type: <b>void*</b>

A pointer to the shared memory block returned by <a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is <b>TRUE</b> and all modified pages within the specified range are written to the disk with low priority. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Call <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to free the memory block.



