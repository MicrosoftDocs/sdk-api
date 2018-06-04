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

# ClearCommBreak function


## -description


Restores character transmission for a specified communications device and places the transmission line in a nonbreak state.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A communications device is placed in a break state by the 
<a href="https://msdn.microsoft.com/997fa1e0-c585-4517-abe7-77b9b08440ee">SetCommBreak</a> or 
<a href="https://msdn.microsoft.com/27c4ebdf-1c06-4a60-8e49-dcccba10789c">EscapeCommFunction</a> function. Character transmission is then suspended until the break state is cleared by calling 
<b>ClearCommBreak</b>.




## -see-also




<a href="https://msdn.microsoft.com/9cc52104-aa5e-4baa-86f1-8c6dcdd661ef">ClearCommError</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/27c4ebdf-1c06-4a60-8e49-dcccba10789c">EscapeCommFunction</a>



<a href="https://msdn.microsoft.com/997fa1e0-c585-4517-abe7-77b9b08440ee">SetCommBreak</a>
 

 

