---
UID: NF:winbase.GetNumaAvailableMemoryNode
title: GetNumaAvailableMemoryNode function
author: windows-driver-content
description: Retrieves the amount of memory available in the specified node.
old-location: base\getnumaavailablememorynode.htm
old-project: ProcThread
ms.assetid: 8db45ec1-fa3c-4395-8986-817e8b137a8a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetNumaAvailableMemoryNode, GetNumaAvailableMemoryNode function, _win32_getnumaavailablememorynode, base.getnumaavailablememorynode, winbase/GetNumaAvailableMemoryNode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	GetNumaAvailableMemoryNode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNumaAvailableMemoryNode function


## -description


Retrieves the amount of memory available in the specified node. 

Use the <a href="https://msdn.microsoft.com/59382114-f3da-45e0-843e-51c0fd52a164">GetNumaAvailableMemoryNodeEx</a> function to specify the node  as a <b>USHORT</b> value.


## -parameters




### -param Node [in]

The number of the node.


### -param AvailableBytes [out]

The amount of available memory for the node, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetNumaAvailableMemoryNode</b> function returns the amount of memory consumed by free and zeroed pages on the specified node. On systems with more than one node, this memory does not include standby pages. Therefore, the sum of the available memory values for all nodes in the system is equal to the value of the Free &amp; Zero Page List Bytes memory performance counter. On systems with only one node, the value returned by <b>GetNumaAvailableMemoryNode</b>  includes standby pages and  is equal to the value of the Available Bytes memory performance counter. For more information about performance counters, see <a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>.




## -see-also




<a href="https://msdn.microsoft.com/59382114-f3da-45e0-843e-51c0fd52a164">GetNumaAvailableMemoryNodeEx</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

