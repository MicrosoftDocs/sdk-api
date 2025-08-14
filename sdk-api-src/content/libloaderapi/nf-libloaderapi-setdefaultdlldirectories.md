---
UID: NF:libloaderapi.SetDefaultDllDirectories
title: SetDefaultDllDirectories function (libloaderapi.h)
description: Specifies a default set of directories to search when the calling process loads a DLL. This search path is used when LoadLibraryEx is called with no LOAD_LIBRARY_SEARCH flags.
helpviewer_keywords: ["LOAD_LIBRARY_SEARCH_APPLICATION_DIR","LOAD_LIBRARY_SEARCH_DEFAULT_DIRS","LOAD_LIBRARY_SEARCH_SYSTEM32","LOAD_LIBRARY_SEARCH_USER_DIRS","SetDefaultDllDirectories","SetDefaultDllDirectories function","base.setdefaultdlldirectories","libloaderapi/SetDefaultDllDirectories"]
old-location: base\setdefaultdlldirectories.htm
tech.root: base
ms.assetid: 66884797-b1c8-4e50-aef1-e88944766d50
ms.date: 12/05/2018
ms.keywords: LOAD_LIBRARY_SEARCH_APPLICATION_DIR, LOAD_LIBRARY_SEARCH_DEFAULT_DIRS, LOAD_LIBRARY_SEARCH_SYSTEM32, LOAD_LIBRARY_SEARCH_USER_DIRS, SetDefaultDllDirectories, SetDefaultDllDirectories function, base.setdefaultdlldirectories, libloaderapi/SetDefaultDllDirectories
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only],KB2533623     on Windows 7, Windows Server 2008 R2, Windows Vista, and     Windows Server 2008
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDefaultDllDirectories
 - libloaderapi/SetDefaultDllDirectories
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - SetDefaultDllDirectories
---

# SetDefaultDllDirectories function


## -description

Specifies a default set of directories to search when the calling process loads a DLL. This search 
    path is used when <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> is called with no 
    <b>LOAD_LIBRARY_SEARCH</b> flags.

## -parameters

### -param DirectoryFlags [in]

The directories to search. This parameter can be any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_APPLICATION_DIR"></a><a id="load_library_search_application_dir"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_APPLICATION_DIR</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If this value is used, the application's installation directory is searched.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_DEFAULT_DIRS"></a><a id="load_library_search_default_dirs"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_DEFAULT_DIRS</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
This value is a combination of <b>LOAD_LIBRARY_SEARCH_APPLICATION_DIR</b>,  
         <b>LOAD_LIBRARY_SEARCH_SYSTEM32</b>, and 
         <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>.

This value represents the recommended maximum number of directories an application should include in its 
         DLL search path.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_SYSTEM32"></a><a id="load_library_search_system32"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_SYSTEM32</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If this value is used, %windows%\system32 is searched.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_USER_DIRS"></a><a id="load_library_search_user_dirs"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_USER_DIRS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If this value is used, any path explicitly added using the 
        <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> or 
        <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function is searched. If more than 
        one directory has been added, the order in which those directories are searched is unspecified.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The DLL search path is the set of directories that are searched for a DLL when a full path is not specified in 
    a <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> or 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> function call, or when a full path to the 
    DLL is specified but the system must search for dependent DLLs. For more information about the standard DLL search 
    path, see 
    <a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>.

The standard DLL search path contains directories that can be vulnerable to a 
    <a href="/windows/desktop/Dlls/dynamic-link-library-security">DLL pre-loading attack</a>. An application can 
    use the <b>SetDefaultDllDirectories</b> function to 
    specify  a default DLL search path for the process that eliminates the most vulnerable directories and limits the 
    other directories that are searched. The process DLL search path applies only to the calling process and persists 
    for the life of the process.

If the <i>DirectoryFlags</i> parameter specifies more than one flag, the directories are 
    searched in the following order:

<ul>
<li>The directory that contains the DLL (<b>LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR</b>). This 
      directory is searched only for dependencies of the DLL being loaded.</li>
<li>The application directory (<b>LOAD_LIBRARY_SEARCH_APPLICATION_DIR</b>).</li>
<li>Paths explicitly added to the application search path with the 
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> function 
      (<b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>) or the 
      <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function. If more than one path has 
      been added, the  order in which the paths are searched is unspecified.</li>
<li>The System directory (<b>LOAD_LIBRARY_SEARCH_SYSTEM32</b>).</li>
</ul>
If <b>SetDefaultDllDirectories</b> does not 
    specify <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>, directories specified with the 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> function are used only for 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> function calls that specify 
    <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>.

It is not possible to revert to the standard DLL search path or remove any directory specified with 
    <b>SetDefaultDllDirectories</b> from the search 
    path. However, the process DLL search path can be overridden by calling 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> with one or more 
    <b>LOAD_LIBRARY_SEARCH</b> flags, and directories added with 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> can be removed by calling 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-removedlldirectory">RemoveDllDirectory</a>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>To call this function in an application, use the 
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to retrieve its address from 
      Kernel32.dll. 
      <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> must be 
      installed on the target platform.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-security">Dynamic-Link Library Security</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-removedlldirectory">RemoveDllDirectory</a>