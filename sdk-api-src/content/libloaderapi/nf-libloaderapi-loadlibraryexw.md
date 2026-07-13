---
UID: NF:libloaderapi.LoadLibraryExW
title: LoadLibraryExW function (libloaderapi.h)
description: Loads the specified module into the address space of the calling process. (LoadLibraryExW)
helpviewer_keywords: ["DONT_RESOLVE_DLL_REFERENCES", "LDR_IS_DATAFILE", "LDR_IS_IMAGEMAPPING", "LDR_IS_RESOURCE", "LOAD_IGNORE_CODE_AUTHZ_LEVEL", "LOAD_LIBRARY_AS_DATAFILE", "LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE", "LOAD_LIBRARY_AS_IMAGE_RESOURCE", "LOAD_LIBRARY_SEARCH_APPLICATION_DIR", "LOAD_LIBRARY_SEARCH_DEFAULT_DIRS", "LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR", "LOAD_LIBRARY_SEARCH_SYSTEM32", "LOAD_LIBRARY_SEARCH_USER_DIRS", "LOAD_WITH_ALTERED_SEARCH_PATH", "LoadLibraryEx", "LoadLibraryEx function", "LoadLibraryExW", "_win32_loadlibraryex", "base.loadlibraryex", "libloaderapi/LoadLibraryEx", "libloaderapi/LoadLibraryExW"]
old-location: base\loadlibraryex.htm
tech.root: base
ms.assetid: 4fc699ca-6ffb-4954-9b72-1b827d558563
ms.date: 07/15/2024
ms.keywords: DONT_RESOLVE_DLL_REFERENCES, LDR_IS_DATAFILE, LDR_IS_IMAGEMAPPING, LDR_IS_RESOURCE, LOAD_IGNORE_CODE_AUTHZ_LEVEL, LOAD_LIBRARY_AS_DATAFILE, LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE, LOAD_LIBRARY_AS_IMAGE_RESOURCE, LOAD_LIBRARY_SEARCH_APPLICATION_DIR, LOAD_LIBRARY_SEARCH_DEFAULT_DIRS, LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR, LOAD_LIBRARY_SEARCH_SYSTEM32, LOAD_LIBRARY_SEARCH_USER_DIRS, LOAD_WITH_ALTERED_SEARCH_PATH, LoadLibraryEx, LoadLibraryEx function, LoadLibraryExA, LoadLibraryExW, _win32_loadlibraryex, base.loadlibraryex, libloaderapi/LoadLibraryEx, libloaderapi/LoadLibraryExA, libloaderapi/LoadLibraryExW, winbase/LoadLibraryEx, winbase/LoadLibraryExA, winbase/LoadLibraryExW
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: LoadLibraryExW (Unicode) and LoadLibraryExA (ANSI)
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - LoadLibraryExW
 - libloaderapi/LoadLibraryExW
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
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - LoadLibraryEx
 - LoadLibraryExA
 - LoadLibraryExW
---

# LoadLibraryExW function


## -description

Loads the specified module into the address space of the calling process. The specified
    module may cause other modules to be loaded.

## -parameters

### -param lpLibFileName [in]

A string that specifies the file name of the module to load. This name is not related to the name stored in a
       library module itself, as specified by the <b>LIBRARY</b> keyword in the module-definition
       (.def) file.

The module can be a library module (a .dll file) or an executable module (an .exe file). If the
       specified module is an executable module, static imports are not loaded; instead, the module is loaded as if
       <b>DONT_RESOLVE_DLL_REFERENCES</b> was specified. See the <i>dwFlags</i>
       parameter for more information.

If the string specifies a module name without a path and the file name extension is omitted, and the module name does
       not contain any point character (.), then the function appends the default library extension ".DLL" to the module name.
       To prevent the function from appending ".DLL" to the module name, include a trailing point character (.) in the module
       name string.

If the string specifies a fully qualified path, the function searches only that path for the module. When
       specifying a path, be sure to use backslashes (\\), not forward slashes (/). For more information about paths,
       see <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

If the string specifies a module name without a path and more than one loaded module has the same base name
       and extension, the function returns a handle to the module that was loaded first.

If the string specifies a module name without a path and a module of the same name is not already loaded, or
       if the string specifies a module name with a relative path, the function searches for the specified module. The
       function also searches for modules if loading the specified module causes the system to load other associated
       modules (that is, if the module has dependencies). The directories that are searched and the order in which
       they are searched depend on the specified path and the <i>dwFlags</i> parameter. For more
       information, see Remarks.

If the function cannot find the  module or one of its dependencies, the function fails.

### -param hFile

This parameter is reserved for future use. It must be <b>NULL</b>.

### -param dwFlags [in]

The action to be taken when loading the module. If no flags are specified, the behavior of this function is
      identical to that of the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function. This
      parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DONT_RESOLVE_DLL_REFERENCES"></a><a id="dont_resolve_dll_references"></a><dl>
<dt><b>DONT_RESOLVE_DLL_REFERENCES</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this value is used, and the executable module is a DLL, the system does not call
         <a href="/windows/desktop/Dlls/dllmain">DllMain</a> for process and thread initialization and
         termination. Also, the system does not load additional executable modules that are referenced by the
         specified module.

<div class="alert"><b>Note</b>  Do not use this value; it is provided only for backward compatibility. If you are planning to access
         only data or resources in the DLL, use <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> or
         <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> or both. Otherwise, load the library as a DLL or
         executable module using the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>
         function.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_IGNORE_CODE_AUTHZ_LEVEL"></a><a id="load_ignore_code_authz_level"></a><dl>
<dt><b>LOAD_IGNORE_CODE_AUTHZ_LEVEL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this value is used, the system does not check
         <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd723678(v=ws.10)">AppLocker</a> rules or apply
         <a href="/previous-versions/windows/it-pro/windows-server-2003/cc779607(v=ws.10)">Software Restriction Policies</a>
         for the DLL. This action applies only to the DLL being loaded and not to its dependencies. This value is
         recommended for use in setup programs that must run extracted DLLs during installation.

<b>Windows Server 2008 R2 and Windows 7:  </b>On systems with KB2532445 installed, the caller must be running as "LocalSystem" or "TrustedInstaller"; otherwise the system ignores this flag. For more information, see "You can circumvent AppLocker rules by using an Office macro on a computer that is running Windows 7 or Windows Server 2008 R2" in the Help and Support Knowledge Base at <a href="https://support.microsoft.com/kb/2532445">https://support.microsoft.com/kb/2532445</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>AppLocker was introduced in Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_AS_DATAFILE"></a><a id="load_library_as_datafile"></a><dl>
<dt><b>LOAD_LIBRARY_AS_DATAFILE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this value is used, the system maps the file into the calling process's virtual address space as if it
         were a data file. Nothing is done to execute or prepare to execute the mapped file. Therefore, you cannot
         call functions like <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a>,
         <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> or
         <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> with this DLL. Using this value
         causes writes to read-only memory to raise an access violation. Use this flag when you want to load a DLL
         only to extract messages or resources from it.

This value can be used with <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b>. For more information,
         see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE"></a><a id="load_library_as_datafile_exclusive"></a><dl>
<dt><b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Similar to <b>LOAD_LIBRARY_AS_DATAFILE</b>, except that the DLL file is opened with
         exclusive write access for the calling process. Other processes cannot open the DLL file for write access
         while it is in use. However, the DLL can still be opened by other processes.

This value can be used with <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b>. For more information,
         see Remarks.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Vista.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_AS_IMAGE_RESOURCE"></a><a id="load_library_as_image_resource"></a><dl>
<dt><b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
If this value is used, the system maps the file into the process's virtual address space as an image file.
         However, the loader does not load the static imports or perform the other usual initialization steps. Use
         this flag when you want to load a DLL only to extract messages or resources from it.

Unless the application depends on the file having the in-memory layout of an image, this value should be used with either
         <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> or
         <b>LOAD_LIBRARY_AS_DATAFILE</b>. For more information, see the Remarks section.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported  until Windows Vista.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_APPLICATION_DIR"></a><a id="load_library_search_application_dir"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_APPLICATION_DIR</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If this value is used, the application's installation directory is searched for the DLL and its
         dependencies. Directories in the standard search path are not searched. This value cannot be combined with
         <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires
          <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> to be
          installed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

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
         <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>. Directories in the standard search path are not
         searched. This value cannot be combined with <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

This value represents the recommended maximum number of directories an application should include in its
         DLL search path.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires
          <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> to be
          installed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR"></a><a id="load_library_search_dll_load_dir"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
If this value is used, the directory that contains the DLL is temporarily added to the beginning of the
         list of directories that are searched for the DLL's dependencies.  Directories in the standard search path
         are not searched.

The <i>lpFileName</i> parameter must specify a fully qualified path. This value cannot
         be combined with <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

For example, if Lib2.dll is a dependency of C:\Dir1\Lib1.dll, loading
         Lib1.dll  with this value causes the system to search for Lib2.dll only in
         C:\Dir1. To search for Lib2.dll in C:\Dir1 and all of the directories
         in the DLL search path, combine this value with <b>LOAD_LIBRARY_DEFAULT_DIRS</b>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires
          <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> to be
          installed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_SYSTEM32"></a><a id="load_library_search_system32"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_SYSTEM32</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If this value is used, %windows%\system32 is searched for the DLL and its dependencies.
         Directories in the standard search path are not searched. This value cannot be combined with
         <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires
          <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> to be
          installed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_LIBRARY_SEARCH_USER_DIRS"></a><a id="load_library_search_user_dirs"></a><dl>
<dt><b>LOAD_LIBRARY_SEARCH_USER_DIRS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If this value is used, directories added using the
         <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> or the
         <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function are searched for the DLL
         and its dependencies. If more than one directory has been added, the order in which the directories are
         searched is unspecified. Directories in the standard search path are not searched. This value cannot be
         combined with <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires
          <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> to be
          installed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_WITH_ALTERED_SEARCH_PATH"></a><a id="load_with_altered_search_path"></a><dl>
<dt><b>LOAD_WITH_ALTERED_SEARCH_PATH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If this value is used and <i>lpFileName</i> specifies an absolute path, the system uses
         the alternate file search strategy discussed in the Remarks section to find associated executable modules
         that the specified module causes to be loaded. If this value is used and <i>lpFileName</i>
         specifies a relative path, the behavior is undefined.

If this value is not used, or if <i>lpFileName</i> does not specify a path, the system
         uses the standard search strategy discussed in the Remarks section to find associated executable modules that
         the specified module causes to be loaded.

This value cannot be combined with any <b>LOAD_LIBRARY_SEARCH</b> flag.

</td>
</tr>

<tr>
<td width="40%"><a id="LOAD_LIBRARY_REQUIRE_SIGNED_TARGET"></a><dl>
<dt><b>LOAD_LIBRARY_REQUIRE_SIGNED_TARGET</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Specifies that the digital signature of the binary image must be checked at load time.

This value requires Windows 8.1, Windows 10 or later.

</td>
</tr>



<tr>
<td width="40%"><a id="LOAD_LIBRARY_SAFE_CURRENT_DIRS"></a><dl>
<dt><b>LOAD_LIBRARY_SAFE_CURRENT_DIRS</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
If this value is used, loading a DLL for execution from the current directory is only allowed if it is under a directory in the Safe load list.

</td>
</tr>

</table>

## -returns

If the function succeeds, the return value is a handle to the loaded module.

If the function fails, the return value is <b>NULL</b>. To get extended error information,
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>LoadLibraryEx</b> function is very similar to the
     <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function. The differences consist of a set of
     optional behaviors that <b>LoadLibraryEx</b> provides:

<ul>
<li><b>LoadLibraryEx</b> can load a DLL module without
      calling the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function of the DLL.</li>
<li><b>LoadLibraryEx</b> can load a module in a way that is
      optimized for the case where the module will never be executed, loading the module as if it were a data
      file.</li>
<li><b>LoadLibraryEx</b> can find modules and their
      associated modules by using  either of two search strategies or it can search a process-specific set of
      directories.</li>
</ul>
You select these optional behaviors by setting the <i>dwFlags</i> parameter; if
     <i>dwFlags</i> is zero,
     <b>LoadLibraryEx</b> behaves identically to
     <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>.

The calling process can use the handle returned by
    <b>LoadLibraryEx</b> to identify the module in calls to the
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>,
    <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>, and
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> functions.

To enable or disable error messages displayed by the loader during DLL loads, use the
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function.

It is not safe to call <b>LoadLibraryEx</b> from
    <a href="/windows/desktop/Dlls/dllmain">DllMain</a>. For more information, see the Remarks section in
    <b>DllMain</b>.

<b>Visual C++:  </b>The Visual C++ compiler supports a syntax that enables you to declare thread-local variables:
      <b>_declspec(thread)</b>. If you use this syntax in a DLL, you will not be able to load the
      DLL explicitly using <b>LoadLibraryEx</b> on versions of
      Windows prior to Windows Vista. If your DLL will be loaded explicitly, you must use the thread
      local storage functions instead of <b>_declspec(thread)</b>. For an example, see
      <a href="/windows/desktop/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage in a Dynamic Link Library</a>.

<h3><a id="Loading_a_DLL_as_a_Data_File_or_Image_Resource"></a><a id="loading_a_dll_as_a_data_file_or_image_resource"></a><a id="LOADING_A_DLL_AS_A_DATA_FILE_OR_IMAGE_RESOURCE"></a>Loading a DLL as a Data File or Image Resource</h3>
The <b>LOAD_LIBRARY_AS_DATAFILE</b>,
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b>, and
      <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> values affect the per-process reference count and the
      loading of the specified module. If any of these values is specified for the <i>dwFlags</i>
      parameter, the loader checks whether the module was already loaded by the process as an executable DLL. If so,
      this means that the module is already mapped into the virtual address space of the calling process. In this
      case, <b>LoadLibraryEx</b> returns a handle to the DLL and
      increments the DLL reference count. If the DLL module was not already loaded as a DLL, the system maps the
      module as a data or image file and not as an executable DLL. In this case,
      <b>LoadLibraryEx</b> returns a handle to the loaded data or
      image file but does not increment the reference count for the module and does not make the module visible to functions such as <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> or <a href="/windows/desktop/api/psapi/nf-psapi-enumprocessmodules">EnumProcessModules</a>.

If <b>LoadLibraryEx</b> is called twice for the same file
      with <b>LOAD_LIBRARY_AS_DATAFILE</b>,
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b>, or
      <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b>, two separate mappings are created for the file.

When the <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> value is used, the module is loaded as an
      image using portable executable (PE) section alignment expansion. Relative virtual addresses (RVA) do not have
      to be mapped to disk addresses, so resources can be more quickly retrieved from the module. Specifying
      <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> prevents other processes from modifying the module
      while it is loaded.

Unless an application depends on specific image mapping characteristics, the
      <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> value should be used with either
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> or
      <b>LOAD_LIBRARY_AS_DATAFILE</b>. This allows the loader to choose whether to load the module
      as an image resource or a data file, selecting whichever option enables the system to share pages more
      effectively. Resource  functions such as
      <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a> can use either mapping.



To determine how a module was loaded, use one of the  following macros to test the handle returned by
      <b>LoadLibraryEx</b>.


```cpp
#define LDR_IS_DATAFILE(handle)      (((ULONG_PTR)(handle)) &  (ULONG_PTR)1)
#define LDR_IS_IMAGEMAPPING(handle)  (((ULONG_PTR)(handle)) & (ULONG_PTR)2)
#define LDR_IS_RESOURCE(handle)      (LDR_IS_IMAGEMAPPING(handle) || LDR_IS_DATAFILE(handle))

```


The following table describes these macros.
      <table>
<tr>
<th>Macro</th>
<th>Description</th>
</tr>
<tr>
<td><b>LDR_IS_DATAFILE</b>(<i>handle</i>)</td>
<td>If this macro returns <b>TRUE</b>, the module was loaded as a data file
         (<b>LOAD_LIBRARY_AS_DATAFILE</b> or
         <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b>).</td>
</tr>
<tr>
<td><b>LDR_IS_IMAGEMAPPING</b>(<i>handle</i>)</td>
<td>If this macro returns <b>TRUE</b>, the module was loaded as an image file
         (<b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b>).</td>
</tr>
<tr>
<td><b>LDR_IS_RESOURCE</b>(<i>handle</i>)</td>
<td>If this macro returns <b>TRUE</b>, the module was loaded as either a data file or an
         image file.</td>
</tr>
</table>
 



Use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function to free a loaded module,
      whether or not loading the module caused its reference count to be incremented. If the module was loaded as a
      data or image file, the mapping is destroyed but the reference count is not decremented. Otherwise, the DLL
      reference count is decremented. Therefore, it is safe to call
      <b>FreeLibrary</b> with any handle returned by
      <b>LoadLibraryEx</b>.

<h3><a id="Searching_for_DLLs_and_Dependencies"></a><a id="searching_for_dlls_and_dependencies"></a><a id="SEARCHING_FOR_DLLS_AND_DEPENDENCIES"></a>Searching for DLLs and Dependencies</h3>
The search path is the set of directories that are searched for a DLL. The
      <b>LoadLibraryEx</b> function can search for a DLL using a
      standard search path or an altered search path, or it can use a process-specific search path established with
      the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-setdefaultdlldirectories">SetDefaultDllDirectories</a> and
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> functions. For a list of directories
      and the order in which they are searched, see
      <a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>.

The <b>LoadLibraryEx</b> function uses the standard search
      path in the following cases:
      <ul>
<li>The file name is specified without a path and the base file name does not match the base file name of a
        loaded module, and none of the <b>LOAD_LIBRARY_SEARCH</b> flags are used.</li>
<li>A path is specified but <b>LOAD_WITH_ALTERED_SEARCH_PATH</b> is not used.</li>
<li>The application has not specified a default DLL search path for the process using
        <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-setdefaultdlldirectories">SetDefaultDllDirectories</a>.</li>
</ul>


If <i>lpFileName</i> specifies a relative path, the entire relative path is appended to
      every token in the DLL search path. To load a module from a relative path without searching any other path, use
      <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> to get a nonrelative path and call
      <b>LoadLibraryEx</b> with the nonrelative path. If the module
      is being loaded as a datafile and the relative path starts with  ".\" or
      "..\", the relative path is treated as an absolute path.

If <i>lpFileName</i> specifies an absolute path and <i>dwFlags</i> is
      set to <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>,
      <b>LoadLibraryEx</b> uses the altered search path.
      The behavior is undefined when <b>LOAD_WITH_ALTERED_SEARCH_PATH</b> flag is set, and <i>lpFileName</i> specifies a relative path.

The <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function can be used to modify
      the search path. This solution is better than using
      <a href="/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory">SetCurrentDirectory</a> or hard-coding the full path
      to the DLL. However, be aware that using
      <b>SetDllDirectory</b> effectively disables safe DLL search
      mode while the specified directory is in the search path and it is not thread safe. If possible, it is best to
      use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> to modify a default process
      search path. For more information, see
      <a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>.

An application can specify the directories to search for a single
      <b>LoadLibraryEx</b> call by using the
      <b>LOAD_LIBRARY_SEARCH_*</b> flags. If more than one
      <b>LOAD_LIBRARY_SEARCH</b> flag is specified, the directories are searched in the following
      order:
      <ul>
<li>The directory that contains the DLL (<b>LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR</b>). This
        directory is searched only for dependencies of the DLL to be loaded.</li>
<li>The application directory (<b>LOAD_LIBRARY_SEARCH_APPLICATION_DIR</b>).</li>
<li>Paths explicitly added to the application search path with the
        <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> function
        (<b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>) or the
        <a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a> function. If more than one path
        has been added, the  order in which the paths are searched is unspecified.</li>
<li>The System32 directory (<b>LOAD_LIBRARY_SEARCH_SYSTEM32</b>).</li>
</ul>


<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>The <b>LOAD_LIBRARY_SEARCH_*</b> flags are available on systems that have
       <a href="https://support.microsoft.com/kb/2533623">KB2533623</a>
       installed. To determine whether the flags are available, use
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to get the address of the
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a>,
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-removedlldirectory">RemoveDllDirectory</a>, or
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-setdefaultdlldirectories">SetDefaultDllDirectories</a> function. If
       <b>GetProcAddress</b> succeeds, the
       <b>LOAD_LIBRARY_SEARCH_*</b> flags can be used with
       <b>LoadLibraryEx</b>.

If the application has used the
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-setdefaultdlldirectories">SetDefaultDllDirectories</a> function to
      establish a DLL search path for the process and none of the <b>LOAD_LIBRARY_SEARCH_*</b>
      flags are used, the <b>LoadLibraryEx</b> function uses the
      process DLL search path instead of the standard search path.

If a path is specified and there is a redirection file associated with the application, the
      <b>LoadLibraryEx</b> function searches for the module in the
      application directory. If the module exists in the application directory,
      <b>LoadLibraryEx</b> ignores the path specification and
      loads the module from the application directory. If the module does not exist in the application directory, the
      function loads the module from the specified directory. For more information, see
      <a href="/windows/desktop/Dlls/dynamic-link-library-redirection">Dynamic Link Library Redirection</a>.

If you call <b>LoadLibraryEx</b> with the name of an
      assembly without a path specification and the assembly is listed in the system compatible manifest, the call is
      automatically redirected to the side-by-side assembly.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
<b>LOAD_LIBRARY_AS_DATAFILE</b> does not prevent other processes from modifying the module
      while it is loaded. Because this can make your application less secure, you should use
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> instead of
      <b>LOAD_LIBRARY_AS_DATAFILE</b> when loading a module as a data file, unless you
      specifically need to use <b>LOAD_LIBRARY_AS_DATAFILE</b>. Specifying
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> prevents other processes from modifying the module
      while it is loaded. Do not specify  <b>LOAD_LIBRARY_AS_DATAFILE</b> and
      <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> in the same call.

Do not use the <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function to retrieve a path to
      a DLL for a subsequent <b>LoadLibraryEx</b> call. The
      <b>SearchPath</b> function uses a different search order than
      <b>LoadLibraryEx</b> and it does not use safe process search
      mode unless this is explicitly enabled by calling
      <a href="/windows/desktop/api/winbase/nf-winbase-setsearchpathmode">SetSearchPathMode</a> with
      <b>BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE</b>. Therefore,
      <b>SearchPath</b> is likely to first search the user's current
      working directory for the specified DLL. If an attacker has copied a malicious version of a DLL into the
      current working directory, the path retrieved by
      <b>SearchPath</b> will point to the malicious DLL, which
      <b>LoadLibraryEx</b> will then load.

Do not make assumptions about the operating system version based on a
      <b>LoadLibraryEx</b> call that searches for a DLL. If the
      application is running in an environment where the DLL is legitimately not present but a malicious version of
      the DLL is in the search path, the malicious version of the DLL may be loaded. Instead, use the recommended
      techniques described in
      <a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

For a general discussion of DLL security issues, see
      <a href="/windows/desktop/Dlls/dynamic-link-library-security">Dynamic-Link Library Security</a>.


#### Examples

For an example, see
     <a href="/windows/desktop/NetMgmt/looking-up-text-for-error-code-numbers">Looking Up Text for Error Code Numbers</a>.

<div class="code"></div>




> [!NOTE]
> The libloaderapi.h header defines LoadLibraryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Dlls/dllmain">DllMain</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-security">Dynamic-Link Library Security</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>



<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>
