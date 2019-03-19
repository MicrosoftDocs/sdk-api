---
UID: NF:errhandlingapi.GetThreadErrorMode
title: GetThreadErrorMode function (errhandlingapi.h)
author: windows-sdk-content
description: Retrieves the error mode for the calling thread.
old-location: base\getthreaderrormode.htm
tech.root: Debug
ms.assetid: 246d838a-ba16-4ba4-8cd3-f25dfc7d2f23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThreadErrorMode, GetThreadErrorMode function, base.getthreaderrormode, errhandlingapi/GetThreadErrorMode
ms.topic: function
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - API-Ms-Win-Core-ErrorHandling-L1-1-3.dll
 - KernelBase.dll
api_name:
 - GetThreadErrorMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadErrorMode function


## -description


Retrieves the error mode for the calling thread. 


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
The system does not display the critical-error-handler message box. Instead, the system sends the error to the calling thread.

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
The system does not display a message box when it fails to find a file. Instead, the error is returned to the calling thread.

</td>
</tr>
</table>
 




## -remarks



A thread inherits the error mode of the process in which it is running. To change the error mode for the thread, use the <a href="https://msdn.microsoft.com/f5acb4ba-d328-47c2-8c41-17df197f12ea">SetThreadErrorMode</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/7673e4ab-bfc8-4c47-b40a-0ae1b4ec5506">GetErrorMode</a>



<a href="https://msdn.microsoft.com/f5acb4ba-d328-47c2-8c41-17df197f12ea">SetThreadErrorMode</a>
 

 

