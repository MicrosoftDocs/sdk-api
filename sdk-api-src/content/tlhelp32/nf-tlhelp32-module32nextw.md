---
UID: NF:tlhelp32.Module32NextW
title: Module32NextW function
author: windows-sdk-content
description: Retrieves information about the next module associated with a process or thread.
old-location: toolhelp\module32next.htm
old-project: ToolHelp
ms.assetid: 88ec1af4-bae7-4cd7-b830-97a98fb337f4
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Module32Next, Module32Next function [ToolHelp], Module32NextW, _win32_module32next, base.module32next, tlhelp32/Module32Next, tlhelp32/Module32NextW, toolhelp.module32next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Module32NextW (Unicode) and Module32Next (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TpcGetSamplesArgs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-toolhelp-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
-	API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
-	Module32Next
-	Module32Next
-	Module32NextW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# Module32NextW function


## -description


Retrieves information about the next module associated with a process or thread.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lpme [out]

A pointer to a 
<a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if the next entry of the module list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if no more modules exist.




## -remarks



To retrieve information about first module associated with a process, use the 
<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/8efe1e13-6222-496a-bff3-90f53b03c750">Traversing the Module List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a>



<a href="https://msdn.microsoft.com/1b539e2f-1326-42aa-af58-ffd7e2833b9b">Module Walking</a>



<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

