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

# RasEapFreeMemory function


## -description


The RAS connection manager calls 
<b>RasEapFreeMemory</b> to free memory buffers returned by 
<a href="https://msdn.microsoft.com/cdd9b081-e654-445e-9383-3665258f5cfa">RasEapInvokeConfigUI</a>, 
<a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a>, and 
<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a>.


## -parameters




### -param pMemory [in]

Pointer to the memory to free.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.




## -remarks



An authentication protocol may implement its various user interfaces in different DLLs. In such a case, each DLL must implement the 
<b>RasEapFreeMemory</b> function.

It is also possible that a single DLL may implement multiple user interfaces. For example, a single DLL may implement both the configuration and identity user interface for an authentication protocol. Another example would be a DLL that implements two configuration user interfaces, each to support a different authentication protocol. In these cases, the DLL must implement a single version of 
<b>RasEapFreeMemory</b> that can free memory returned from any of the user interfaces implemented in the DLL.




## -see-also




<a href="https://msdn.microsoft.com/090a3620-3732-4466-95ac-ce9cbdd36484">EAP Functions</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a>



<a href="https://msdn.microsoft.com/cdd9b081-e654-445e-9383-3665258f5cfa">RasEapInvokeConfigUI</a>



<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a>
 

 

