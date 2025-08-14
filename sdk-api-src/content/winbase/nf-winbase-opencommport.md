---
UID: NF:winbase.OpenCommPort
title: OpenCommPort function (winbase.h)
description: Attempts to open a communication device.
helpviewer_keywords: ["FILE_FLAG_OVERLAPPED","OpenCommPort","OpenCommPort function","base.opencommport","winbase/OpenCommPort"]
old-location: base\opencommport.htm
tech.root: base
ms.assetid: D96D3F6D-2158-4E6A-84A8-DC3BAE9624FA
ms.date: 12/05/2018
ms.keywords: FILE_FLAG_OVERLAPPED, OpenCommPort, OpenCommPort function, base.opencommport, winbase/OpenCommPort
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
req.lib: OneCore.lib
req.dll: KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenCommPort
 - winbase/OpenCommPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - OpenCommPort
---

# OpenCommPort function


## -description

Attempts to open a communication device.

## -parameters

### -param uPortNumber [in]

A one-based port number for the communication device to open.

### -param dwDesiredAccess [in]

The requested access to the device.

For more information about requested access, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> and <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

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

If the function succeeds, the function returns a valid <b>HANDLE</b>. Use <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close that handle.

If an error occurs, the function returns <b>INVALID_HANDLE_VALUE</b>.

## -remarks

The <i>uPortNumber</i> parameter accepts one-based values. A value of 1 for <i>uPortNumber</i> causes this function to attempt to open COM1.

To support UWP, link against WindowsApp.lib.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>