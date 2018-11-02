---
UID: NF:winbase.QueryFullProcessImageNameW
title: QueryFullProcessImageNameW function
author: windows-sdk-content
description: Retrieves the full name of the executable image for the specified process.
old-location: base\queryfullprocessimagename.htm
tech.root: procthread
ms.assetid: 49a9d1aa-30f3-45ea-a4ec-9f55df692b8b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PROCESS_NAME_NATIVE, QueryFullProcessImageName, QueryFullProcessImageName function, QueryFullProcessImageNameA, QueryFullProcessImageNameW, base.queryfullprocessimagename, winbase/QueryFullProcessImageName, winbase/QueryFullProcessImageNameA, winbase/QueryFullProcessImageNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryFullProcessImageNameW (Unicode) and QueryFullProcessImageNameA (ANSI)
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
 - API-MS-Win-Core-psapi-ansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-psapi-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - QueryFullProcessImageName
 - QueryFullProcessImageNameA
 - QueryFullProcessImageNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryFullProcessImageNameW function


## -description


Retrieves the full name of the executable image for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must be created with the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param dwFlags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The name should use the Win32 path format.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_NAME_NATIVE"></a><a id="process_name_native"></a><dl>
<dt><b>PROCESS_NAME_NATIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The name should use the native system path format.

</td>
</tr>
</table>
 


### -param lpExeName [out]

The path to the executable image. If the function succeeds, this string is null-terminated.


### -param lpdwSize [in, out]

On input, specifies the size of the <i>lpExeName</i> buffer, in characters. On success, receives the number of characters written to the buffer, not including the null-terminating character.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/4199ce12-e82f-4a58-ac66-e0ddc0dffbff">GetModuleFileNameEx</a>



<a href="https://msdn.microsoft.com/819fc2f4-0801-417b-9cbb-d7fd2894634e">GetProcessImageFileName</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

