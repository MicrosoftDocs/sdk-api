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

# IApiTracingDataCollector::put_IncludeModules


## -description


Retrieves or sets the list of modules to include in the trace.

This property is read/write.


## -parameters


## -remarks



If you do not set this property, the trace will  include the following modules:

<ul>
<li>Advapi32.dll</li>
<li>Gdi32.dll</li>
<li>Kernel32.dll</li>
<li>User32.dll</li>
</ul>
This property  limits the  trace to a subset of those DLLs. For example, you can use this property to limit the trace to only Kernel32.dll and Advapi32.dll.




## -see-also




<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>



<a href="https://msdn.microsoft.com/aa2239f0-b70e-491f-8a88-b41d429e8bb2">IApiTracingDataCollector::ExePath</a>
 

 

