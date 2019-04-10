---
UID: NF:systemtopologyapi.GetNumaHighestNodeNumber
title: GetNumaHighestNodeNumber function (systemtopologyapi.h)
author: windows-sdk-content
description: Retrieves the node that currently has the highest number.
old-location: base\getnumahighestnodenumber.htm
tech.root: ProcThread
ms.assetid: ce944fa7-b42a-4b99-ac8d-30bd026fba21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNumaHighestNodeNumber, GetNumaHighestNodeNumber function, _win32_getnumahighestnodenumber, base.getnumahighestnodenumber, systemtopologyapi/GetNumaHighestNodeNumber, winbase/GetNumaHighestNodeNumber
ms.topic: function
req.header: systemtopologyapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-systemtopology-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-MS-Win-Core-Systemtopology-L1-1-1.dll
api_name:
 - GetNumaHighestNodeNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumaHighestNodeNumber function


## -description


Retrieves the node that currently has the highest number.


## -parameters




### -param HighestNodeNumber [out]

The number of the highest node.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The number of the highest node is not guaranteed to be the total number of nodes.

To retrieve a list of all processors in a node, use the 
<a href="https://msdn.microsoft.com/bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8">GetNumaNodeProcessorMask</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/df025b35-fb6b-4987-806e-9c76e6b130a1">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bdaecb36-9b51-4cc3-88b3-0dbd63bdc9b8">GetNumaNodeProcessorMask</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

