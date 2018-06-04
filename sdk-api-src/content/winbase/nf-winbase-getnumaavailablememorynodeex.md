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

# GetNumaAvailableMemoryNodeEx function


## -description


Retrieves the amount of memory that is available in a node specified as a <b>USHORT</b> value.


## -parameters




### -param Node [in]

The number of the node.


### -param AvailableBytes [out]

The amount of available memory for the node, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetNumaAvailableMemoryNodeEx</b> function returns the amount of memory consumed by free and zeroed pages on the specified node. On systems with more than one node, this memory does not include standby pages. Therefore, the sum of the available memory values for all nodes in the system is equal to the value of the Free &amp; Zero Page List Bytes memory performance counter. On systems with only one node, the value returned by <a href="https://msdn.microsoft.com/8db45ec1-fa3c-4395-8986-817e8b137a8a">GetNumaAvailableMemoryNode</a>  includes standby pages and  is equal to the value of the Available Bytes memory performance counter. For more information about performance counters, see <a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>.

The only difference between the <b>GetNumaAvailableMemoryNodeEx</b> function and the <a href="https://msdn.microsoft.com/8db45ec1-fa3c-4395-8986-817e8b137a8a">GetNumaAvailableMemoryNode</a> function is the data type of the <i>Node</i> parameter. 

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8db45ec1-fa3c-4395-8986-817e8b137a8a">GetNumaAvailableMemoryNode</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>
 

 

