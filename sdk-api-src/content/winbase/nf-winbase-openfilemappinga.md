---
UID: NF:winbase.OpenFileMappingA
title: OpenFileMappingA function (winbase.h)
author: windows-sdk-content
description: Opens a named file mapping object.
old-location: base\openfilemapping.htm
tech.root: Memory
ms.assetid: 4896144c-78fc-4d21-a302-d9ba66fb2f8a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenFileMapping, OpenFileMapping function, OpenFileMappingA, OpenFileMappingW, _win32_openfilemapping, base.openfilemapping, fs.openfilemapping, winbase/OpenFileMapping, winbase/OpenFileMappingA, winbase/OpenFileMappingW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenFileMappingW (Unicode) and OpenFileMappingA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - OpenFileMapping
 - OpenFileMappingA
 - OpenFileMappingW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenFileMappingA function


## -description


Opens a named file mapping object.


## -parameters




### -param dwDesiredAccess [in]

The access to the file mapping object. This access is checked against any security descriptor on the target 
      file mapping object. For a list of values, see 
      <a href="https://msdn.microsoft.com/8bbf7c98-ff83-4ed9-8b82-f08dcd31295c">File Mapping Security and Access Rights</a>.


### -param bInheritHandle [in]

If this parameter is <b>TRUE</b>, a process created by the 
      <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function can inherit the handle; 
      otherwise, the handle cannot be inherited.


### -param lpName [in]

The name of the file mapping object to be opened. If there is an open handle to a file mapping object by 
      this name and the security descriptor on the mapping object does not conflict with the 
      <i>dwDesiredAccess</i> parameter, the open operation succeeds. The name can have a 
      "Global\" or "Local\" prefix to explicitly open an object in the global or 
      session namespace. The remainder of the name can contain any character except the backslash character (\). For 
      more information, see 
      <a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user 
      switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next 
      user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal 
      Services so that applications can support multiple users.


## -returns



If the function succeeds, the return value is an open handle to the specified file mapping object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The handle that <b>OpenFileMapping</b> returns can be used 
     with any function that requires a handle to a file mapping object.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
     If required, the caller should use <a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> to set the 
     timestamp.

When it is no longer needed, the caller should call release the handle returned by 
     <b>OpenFileMapping</b> with a call to 
     <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.

In Windows Server 2012, this function is supported by the following technologies.

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
     <a href="https://msdn.microsoft.com/17458be2-3ef7-42f2-a717-abf73ac4846f">Creating Named Shared Memory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">File Mapping Functions</a>



Memory Management Functions



<a href="https://msdn.microsoft.com/942cb50d-df07-444f-bba5-58194556ae66">Sharing Files and Memory</a>
 

 

