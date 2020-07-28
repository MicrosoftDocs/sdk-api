---
UID: NF:memoryapi.OpenFileMappingFromApp
title: OpenFileMappingFromApp function (memoryapi.h)
description: Opens a named file mapping object.
helpviewer_keywords: ["OpenFileMappingFromApp","OpenFileMappingFromApp function","base.openfilemappingfromapp","memoryapi/OpenFileMappingFromApp"]
old-location: base\openfilemappingfromapp.htm
tech.root: base
ms.assetid: 66BAB9A6-F983-49D8-8F87-69A3CCBBB1BC
ms.date: 12/05/2018
ms.keywords: OpenFileMappingFromApp, OpenFileMappingFromApp function, base.openfilemappingfromapp, memoryapi/OpenFileMappingFromApp
f1_keywords:
- memoryapi/OpenFileMappingFromApp
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenFileMappingFromApp function


## -description


Opens a named file mapping object.


## -parameters




### -param DesiredAccess [in]

The access to the file mapping object. This access is checked against any security descriptor on the target 
      file mapping object. For a list of values, see 
      <a href="https://docs.microsoft.com/windows/desktop/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>. You can only open the file mapping object for <b>FILE_MAP_EXECUTE</b> access if your app has the <b>codeGeneration</b> capability.


### -param InheritHandle [in]

If this parameter is <b>TRUE</b>, a process created by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit the handle; 
      otherwise, the handle cannot be inherited.


### -param Name [in]

The name of the file mapping object to be opened. If there is an open handle to a file mapping object by 
      this name and the security descriptor on the mapping object does not conflict with the 
      <i>DesiredAccess</i> parameter, the open operation succeeds. The name can have a 
      "Global\" or "Local\" prefix to explicitly open an object in the global or 
      session namespace. The remainder of the name can contain any character except the backslash character (\). For 
      more information, see 
      <a href="https://docs.microsoft.com/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user 
      switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next 
      user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal 
      Services so that applications can support multiple users.


## -returns



If the function succeeds, the return value is an open handle to the specified file mapping object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



You can call <b>OpenFileMappingFromApp</b> from Windows Store apps with just-in-time (JIT) capabilities to use JIT functionality. The app must include the <b>codeGeneration</b> capability in the app manifest file to use JIT capabilities. <b>OpenFileMappingFromApp</b> lets Windows Store apps use the <a href="https://docs.microsoft.com/dotnet/api/system.io.memorymappedfiles.memorymappedfile?redirectedfrom=MSDN">MemoryMappedFile</a> class in the .NET Framework.

The handle that <b>OpenFileMappingFromApp</b> returns can be used 
     with any function that requires a handle to a file mapping object.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
     If required, the caller should use <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> to set the 
     timestamp.

When it is no longer needed, the caller should call release the handle returned by 
     <b>OpenFileMappingFromApp</b> with a call to 
     <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">File Mapping Functions</a>



Memory Management Functions



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/sharing-files-and-memory">Sharing Files and Memory</a>
 

 

