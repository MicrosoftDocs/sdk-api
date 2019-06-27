---
UID: NF:fileapi.FindFirstFileNameW
title: FindFirstFileNameW function (fileapi.h)
author: windows-sdk-content
description: Creates an enumeration of all the hard links to the specified file. The FindFirstFileNameW function returns a handle to the enumeration that can be used on subsequent calls to the FindNextFileNameW function.
old-location: fs\findfirstfilenamew.htm
tech.root: FileIO
ms.assetid: 9f64aa3e-4c73-47a8-8304-6134f1b4d153
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindFirstFileNameW, FindFirstFileNameW function [Files], fileapi/FindFirstFileNameW, fs.findfirstfilenamew
ms.topic: function
f1_keywords: 
 - "fileapi/FindFirstFileNameW"
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
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
 - API-MS-Win-Core-File-L1-2-2.dll
 - KernelBase.dll
api_name:
 - FindFirstFileNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindFirstFileNameW function


## -description


Creates an enumeration of all the hard links to the specified file. The 
    <b>FindFirstFileNameW</b> function returns a handle to the 
    enumeration that can be used on subsequent calls to the 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findfirstfilenametransactedw">FindFirstFileNameTransactedW</a> function.


## -parameters




### -param lpFileName [in]

The name of the file.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param dwFlags [in]

Reserved; specify zero (0).


### -param StringLength [in, out]

The size of the buffer pointed to by the <i>LinkName</i> parameter, in characters. If 
      this call fails and the error returned from the 
      <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function is 
      <b>ERROR_MORE_DATA</b> (234), the value that is returned by this parameter is the size that 
      the buffer pointed to by <i>LinkName</i>  must be to contain all the data.


### -param LinkName [in, out]

A pointer to a buffer to store the first link name found for <i>lpFileName</i>.


## -returns



If the function succeeds, the return value is a search handle that can be used with the 
       <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a> function or closed with the 
       <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b> (0xffffffff). To 
       get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       function.




## -remarks



In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findfirstfilenametransactedw">FindFirstFileNameTransactedW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew">FindNextFileNameW</a>
 

 

