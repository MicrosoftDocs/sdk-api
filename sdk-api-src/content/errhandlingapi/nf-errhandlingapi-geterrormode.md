---
UID: NF:errhandlingapi.GetErrorMode
title: GetErrorMode function (errhandlingapi.h)
author: windows-sdk-content
description: Retrieves the error mode for the current process.
old-location: base\geterrormode.htm
tech.root: Debug
ms.assetid: 7673e4ab-bfc8-4c47-b40a-0ae1b4ec5506
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetErrorMode, GetErrorMode function, base.geterrormode, errhandlingapi/GetErrorMode
ms.topic: function
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - API-MS-Win-Core-errorhandling-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
api_name:
 - GetErrorMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetErrorMode function


## -description


Retrieves the error mode for the current process.


## -parameters






## -returns



The process error mode. This function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEM_FAILCRITICALERRORS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The system does not display the critical-error-handler message box. Instead, the system sends the error 
        to the calling process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEM_NOALIGNMENTFAULTEXCEPT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The system automatically fixes memory alignment faults and makes them invisible to the application. It 
        does this for the calling process and any descendant processes. This feature is only supported by certain 
        processor architectures. For more information, see 
        <a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEM_NOGPFAULTERRORBOX</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The system does not display the Windows Error Reporting dialog.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEM_NOOPENFILEERRORBOX</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The system does not display a message box when it fails to find a file. Instead, the error is returned to 
        the calling process.

</td>
</tr>
</table>
 




## -remarks



Each process has an associated error mode that indicates to the system how the application is going to respond 
    to serious errors. A child process inherits the error mode of its parent process.

To change the error mode for the process, use the 
    <a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a> function.

<b>Windows 7:  </b>Callers should favor <a href="https://msdn.microsoft.com/f5acb4ba-d328-47c2-8c41-17df197f12ea">SetThreadErrorMode</a> over 
      <a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a> since it is less disruptive to the normal 
      behavior of the system. <a href="https://msdn.microsoft.com/246d838a-ba16-4ba4-8cd3-f25dfc7d2f23">GetThreadErrorMode</a> is the 
      call function that corresponds to <b>GetErrorMode</b>.






## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/288be838-6094-4824-9cae-99b7ff9eea74">Error Mode</a>



<a href="https://msdn.microsoft.com/246d838a-ba16-4ba4-8cd3-f25dfc7d2f23">GetThreadErrorMode</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>
 

 

