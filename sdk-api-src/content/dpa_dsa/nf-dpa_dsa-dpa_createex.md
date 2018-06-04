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

# DPA_CreateEx function


## -description


Creates a dynamic pointer array (DPA) using a given specified size and heap location.


## -parameters




### -param cpGrow [in]

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.


### -param hheap [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a></b>

A handle to the heap where the array is stored.


## -returns



Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.




## -remarks



<b>DPA_CreateEx</b> is not exported by name. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 340 from ComCtl32.dll to obtain a function pointer.




## -see-also




<a href="https://msdn.microsoft.com/03bbfe08-69df-41da-85c8-41a96d9dac09">DPA_Create</a>
 

 

