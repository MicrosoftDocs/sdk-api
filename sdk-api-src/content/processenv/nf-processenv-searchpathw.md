---
UID: NF:processenv.SearchPathW
title: SearchPathW function
author: windows-sdk-content
description: Searches for a specified file in a specified path.
old-location: fs\searchpath.htm
tech.root: FileIO
ms.assetid: 8039365a-1b39-431e-af87-9a9933ca102d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SearchPath, SearchPath function [Files], SearchPathA, SearchPathW, _win32_searchpath, base.searchpath, fs.searchpath, processenv/SearchPath, processenv/SearchPathA, processenv/SearchPathW
ms.topic: function
req.header: processenv.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SearchPathW (Unicode) and SearchPathA (ANSI)
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
 - API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SearchPath
 - SearchPathA
 - SearchPathW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SearchPathW function


## -description


Searches for a specified file in a specified path.


## -parameters




### -param lpPath [in, optional]

The path to be searched for the file.

If this parameter is <b>NULL</b>, the 
       function searches for a matching file using a registry-dependent system  search path. For more information, see 
       the Remarks section.


### -param lpFileName [in]

The name of the file for which to search.


### -param lpExtension [in, optional]

The extension to be added to the file name when searching for the file. The first character of the file name 
       extension must be a period (.). The extension is added only if the specified file name does not end with an 
       extension.

If a file name extension is not required or if the file name contains an extension, this parameter can be 
       <b>NULL</b>.


### -param nBufferLength [in]

The size of the buffer that receives the valid path and file name (including the terminating null 
      character), in <b>TCHARs</b>.


### -param lpBuffer [out]

A pointer to the buffer to receive the path and file name of the file found. The  string is a 
      null-terminated string.


### -param lpFilePart [out, optional]

A pointer to the variable to receive the address (within <i>lpBuffer</i>) of the last 
      component of the valid path and file name, which is the address of the character immediately following the final 
      backslash (\) in the path.


## -returns



If the function succeeds, the value returned is the length, in <b>TCHARs</b>, of the 
       string that is copied to the buffer, not including the terminating null character. If the return value is 
       greater than <i>nBufferLength</i>, the value returned is the size of the buffer that is 
       required to hold the path, including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>lpPath</i> parameter is <b>NULL</b>, 
     <b>SearchPath</b> searches for a matching file based on the current 
     value of the following registry value:


<b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Control</b>\<b>Session Manager</b>\<b>SafeProcessSearchMode</b>



When the value of this <b>REG_DWORD</b> registry value is set to 1, 
     <b>SearchPath</b> first searches the folders that are specified in 
     the system path, and then searches the current working folder. When the value of this registry value is set to 0, 
     the computer first searches the current working folder, and then searches the folders that are specified in the 
     system path. The system default value for this registry key is 0.

The search mode used by the <b>SearchPath</b> function can also 
     be set per-process by calling the <a href="https://msdn.microsoft.com/1874933d-92c3-4945-a3e4-e6dede232d5e">SetSearchPathMode</a> 
     function.

The <b>SearchPath</b> function is not recommended as a method of 
     locating a .dll file if the intended use of the output is in a call to the 
     <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function. This can result in locating the 
     wrong .dll file because the search order of the <b>SearchPath</b> 
     function differs from the search order used by the 
     <b>LoadLibrary</b> function. If you need to locate and load a 
     .dll file, use the <b>LoadLibrary</b> function. 

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>SearchPathW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation. See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>
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
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/1874933d-92c3-4945-a3e4-e6dede232d5e">SetSearchPathMode</a>
 

 

