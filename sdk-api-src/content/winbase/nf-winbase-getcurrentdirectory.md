---
UID: NF:winbase.GetCurrentDirectory
title: GetCurrentDirectory function
author: windows-sdk-content
description: Retrieves the current directory for the current process.
old-location: fs\getcurrentdirectory.htm
old-project: fileio
ms.assetid: 1fbe6289-2ca8-4ca8-b004-ecf513f9b0bd
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: GetCurrentDirectory, GetCurrentDirectory function [Files], GetCurrentDirectoryA, GetCurrentDirectoryW, _win32_getcurrentdirectory, base.getcurrentdirectory, fs.getcurrentdirectory, winbase/GetCurrentDirectory, winbase/GetCurrentDirectoryA, winbase/GetCurrentDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCurrentDirectoryW (Unicode) and GetCurrentDirectoryA (ANSI)
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
 - API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCurrentDirectory
 - GetCurrentDirectoryA
 - GetCurrentDirectoryW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCurrentDirectory function


## -description


Retrieves the current directory for the current process.


## -parameters




### -param nBufferLength [in]

The length of the buffer for the current directory string, in <b>TCHARs</b>. The 
      buffer length must include room for a terminating null character.


### -param lpBuffer [out]

A pointer to the buffer that receives the current directory string. This null-terminated string specifies the 
       absolute path to the current directory.

To determine the required buffer size, set this parameter to <b>NULL</b> and the 
       <i>nBufferLength</i> parameter to 0.


## -returns



If the function succeeds, the return value specifies the number of characters that are written to the buffer, 
       not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the buffer that is pointed to by <i>lpBuffer</i> is not large enough, the return value 
       specifies the required size of the buffer, in characters, including the null-terminating character.




## -remarks



Each process has a single current directory that consists of two parts:

<ul>
<li>A disk designator that is either a drive letter followed by a colon, or a server name followed by a share 
      name (\\<i>servername</i>\<i>sharename</i>)</li>
<li>A directory on the disk designator</li>
</ul>
To set the current directory, use the 
    <a href="https://msdn.microsoft.com/02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd">SetCurrentDirectory</a> function.

Multithreaded applications and shared library code should not use the   
    <b>GetCurrentDirectory</b> function and should avoid using relative path names. The current directory state written by the <a href="https://msdn.microsoft.com/02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd">SetCurrentDirectory</a> function is stored as a global variable in each process, therefore multithreaded applications cannot reliably use this value without possible data corruption from other threads that may also be reading or setting this value. This limitation also applies to the <b>SetCurrentDirectory</b> and <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a> functions. The exception being when the application is guaranteed to be running in a single thread, for example parsing file names from the command line argument string in the main thread prior to creating any additional threads. Using relative path names in multithreaded applications or shared library code can yield unpredictable results and is not supported.

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

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
 


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/b08e7739-55d4-4690-9ce5-2a8cb29214e9">Changing the Current Directory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f8ca8b10-c8bd-4285-8a40-dbec4c24729c">CreateDirectory</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a>



<a href="https://msdn.microsoft.com/02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd">SetCurrentDirectory</a>
 

 

