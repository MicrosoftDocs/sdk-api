---
UID: NF:winbase.GetNumaAvailableMemoryNodeEx
title: GetNumaAvailableMemoryNodeEx function (winbase.h)
author: windows-sdk-content
description: Retrieves the amount of memory that is available in a node specified as a USHORT value.
old-location: base\getnumaavailablememorynodeex.htm
tech.root: ProcThread
ms.assetid: 59382114-f3da-45e0-843e-51c0fd52a164
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNumaAvailableMemoryNodeEx, GetNumaAvailableMemoryNodeEx function, base.getnumaavailablememorynodeex, winbase/GetNumaAvailableMemoryNodeEx
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetNumaAvailableMemoryNodeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

