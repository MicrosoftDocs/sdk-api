---
UID: NF:winbase.OpenCommPort
title: OpenCommPort function
author: windows-sdk-content
description: Attempts to open a communication device.
old-location: base\opencommport.htm
old-project: devio
ms.assetid: D96D3F6D-2158-4E6A-84A8-DC3BAE9624FA
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FILE_FLAG_OVERLAPPED, OpenCommPort, OpenCommPort function, base.opencommport, winbase/OpenCommPort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - OpenCommPort
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OpenCommPort function


## -description


Attempts to open a communication device.


## -parameters




### -param uPortNumber [in]

A one-based port number for the communication device to open.


### -param dwDesiredAccess [in]

The requested access to the device.

For more information about requested access, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> and <a href="https://msdn.microsoft.com/094cac29-c66d-409e-8928-878dc693d393">Creating and Opening Files</a>.


### -param dwFlagsAndAttributes [in]

The requested flags and attributes to the device. 

<div class="alert"><b>Note</b>  <p class="note">For this function, only values of <b>FILE_FLAG_OVERLAPPED</b> or 0x0 are expected for this parameter. 

</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OVERLAPPED"></a><a id="file_flag_overlapped"></a><dl>
<dt><b>FILE_FLAG_OVERLAPPED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The file or device is being opened or created for asynchronous I/O.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns a valid <b>HANDLE</b>. Use <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> to close that handle.

If an error occurs, the function returns <b>INVALID_HANDLE_VALUE</b>. 




## -remarks



The <i>uPortNumber</i> parameter accepts one-based values. A value of 1 for <i>uPortNumber</i> causes this function to attempt to open COM1.

To support UWP, link against WindowsApp.lib. 




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/094cac29-c66d-409e-8928-878dc693d393">Creating and Opening Files</a>
 

 

