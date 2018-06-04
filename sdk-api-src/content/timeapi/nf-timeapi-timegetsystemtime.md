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

# timeGetSystemTime function


## -description



The <b>timeGetSystemTime</b> function retrieves the system time, in milliseconds. The system time is the time elapsed since Windows was started. This function works very much like the <a href="https://msdn.microsoft.com/f9d3a7a9-1457-4993-92f1-f888780a565e">timeGetTime</a> function. See <b>timeGetTime</b> for details of these functions' operation.




## -parameters




### -param pmmt


            Pointer to an <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.
          


### -param cbmmt


            Size, in bytes, of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.
          


## -returns



If successful, returns <b>TIMERR_NOERROR</b>. Otherwise, returns an error code.




## -remarks



The system time is returned in the <b>ms</b> member of the <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>
 

 

