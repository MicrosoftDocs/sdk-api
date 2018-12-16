---
UID: NF:memoryapi.OpenFileMappingFromApp
title: OpenFileMappingFromApp function
author: windows-sdk-content
description: Opens a named file mapping object.
old-location: base\openfilemappingfromapp.htm
tech.root: memory
ms.assetid: 66BAB9A6-F983-49D8-8F87-69A3CCBBB1BC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenFileMappingFromApp, OpenFileMappingFromApp function, base.openfilemappingfromapp, memoryapi/OpenFileMappingFromApp
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-memory-l1-1-3.dll
 - KernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - OpenFileMappingFromApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenFileMappingFromApp function


## -description


Opens a named file mapping object.


## -parameters




### -param DesiredAccess [in]

The access to the file mapping object. This access is checked against any security descriptor on the target 
      file mapping object. For a list of values, see 
      <a href="https://msdn.microsoft.com/8bbf7c98-ff83-4ed9-8b82-f08dcd31295c">File Mapping Security and Access Rights</a>. You can only open the file mapping object for <b>FILE_MAP_EXECUTE</b> access if your app has the <b>codeGeneration</b> capability.


### -param InheritHandle [in]

If this parameter is <b>TRUE</b>, a process created by the 
      <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function can inherit the handle; 
      otherwise, the handle cannot be inherited.


### -param Name [in]

The name of the file mapping object to be opened. If there is an open handle to a file mapping object by 
      this name and the security descriptor on the mapping object does not conflict with the 
      <i>DesiredAccess</i> parameter, the open operation succeeds. The name can have a 
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



You can call <b>OpenFileMappingFromApp</b> from Windows Store apps with just-in-time (JIT) capabilities to use JIT functionality. The app must include the <b>codeGeneration</b> capability in the app manifest file to use JIT capabilities. <b>OpenFileMappingFromApp</b> lets Windows Store apps use the <a href="https://msdn.microsoft.com/library/Dd267535(v=VS.100).aspx">MemoryMappedFile</a> class in the .NET Framework.

The handle that <b>OpenFileMappingFromApp</b> returns can be used 
     with any function that requires a handle to a file mapping object.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
     If required, the caller should use <a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> to set the 
     timestamp.

When it is no longer needed, the caller should call release the handle returned by 
     <b>OpenFileMappingFromApp</b> with a call to 
     <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">File Mapping Functions</a>



Memory Management Functions



<a href="https://msdn.microsoft.com/4896144c-78fc-4d21-a302-d9ba66fb2f8a">OpenFileMapping</a>



<a href="https://msdn.microsoft.com/942cb50d-df07-444f-bba5-58194556ae66">Sharing Files and Memory</a>
 

 

