---
UID: NF:libloaderapi.LoadLibraryExA
title: LoadLibraryExA function
author: windows-sdk-content
description: Loads the specified module into the address space of the calling process.
old-location: base\loadlibraryex.htm
tech.root: dlls
ms.assetid: 4fc699ca-6ffb-4954-9b72-1b827d558563
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: DONT_RESOLVE_DLL_REFERENCES, LDR_IS_DATAFILE, LDR_IS_IMAGEMAPPING, LDR_IS_RESOURCE, LOAD_IGNORE_CODE_AUTHZ_LEVEL, LOAD_LIBRARY_AS_DATAFILE, LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE, LOAD_LIBRARY_AS_IMAGE_RESOURCE, LOAD_LIBRARY_SEARCH_APPLICATION_DIR, LOAD_LIBRARY_SEARCH_DEFAULT_DIRS, LOAD_LIBRARY_SEARCH_DLL_LOAD_DIR, LOAD_LIBRARY_SEARCH_SYSTEM32, LOAD_LIBRARY_SEARCH_USER_DIRS, LOAD_WITH_ALTERED_SEARCH_PATH, LoadLibraryEx, LoadLibraryEx function, LoadLibraryExA, LoadLibraryExW, _win32_loadlibraryex, base.loadlibraryex, libloaderapi/LoadLibraryEx, libloaderapi/LoadLibraryExA, libloaderapi/LoadLibraryExW, winbase/LoadLibraryEx, winbase/LoadLibraryExA, winbase/LoadLibraryExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadLibraryExA function


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

If the string specifies a module name without a path and the file name extension is omitted, the function 
       appends the default library extension .dll to the module name. To prevent the function from appending 
       .dll to the module name, include a trailing point character (.) in the module name string.

If the string specifies a fully qualified path, the function searches only that path for the module. When 
       specifying a path, be sure to use backslashes (\), not forward slashes (/). For more information about paths, 
       see <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.

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
      identical to that of the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function. This 
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
         <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> for process and thread initialization and 
         termination. Also, the system does not load additional executable modules that are referenced by the 
         specified module.

<div class="alert"><b>Note</b>  Do not use this value; it is provided only for backward compatibility. If you are planning to access 
         only data or resources in the DLL, use <b>LOAD_LIBRARY_AS_DATAFILE_EXCLUSIVE</b> or 
         <b>LOAD_LIBRARY_AS_IMAGE_RESOURCE</b> or both. Otherwise, load the library as a DLL or 
         executable module using the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> 
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
         <a href="Http://go.microsoft.com/fwlink/p/?linkid=161970">AppLocker</a> rules or apply 
         <a href="Http://go.microsoft.com/fwlink/p/?linkid=161971">Software Restriction Policies</a> 
         for the DLL. This action applies only to the DLL being loaded and not to its dependencies. This value is 
         recommended for use in setup programs that must run extracted DLLs during installation.

<b>Windows Server 2008 R2 and Windows 7:  </b>On systems with KB2532445 installed, the caller must be running as "LocalSystem" or 
          "TrustedInstaller"; otherwise the system ignores this flag. For more information, see 
          "You can circumvent AppLocker rules by using an Office macro on a computer that is running Windows 7 or Windows Server 2008 R2" 
          in the Help and Support Knowledge Base at 
          <a href="Http://support.microsoft.com/kb/2532445">http://support.microsoft.com/kb/2532445</a>.

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
         call functions like <a href="https://msdn.microsoft.com/f124c99f-8be1-4a9c-a84c-b1b323921f1a">GetModuleFileName</a>,  
         <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> or 
         <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> with this DLL. Using this value 
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
          <a href="http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> to be 
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
          <a href="Http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> to be 
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
          <a href="http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> to be 
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
          <a href="Http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> to be 
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
         <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> or the 
         <a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a> function are searched for the DLL 
         and its dependencies. If more than one directory has been added, the order in which the directories are 
         searched is unspecified. Directories in the standard search path are not searched. This value cannot be 
         combined with <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>This value requires 
          <a href="Http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> to be 
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
</table>
 


## -returns



If the function succeeds, the return value is a handle to the loaded module.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>LoadLibraryEx</b> function is very similar to the 
     <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function. The differences consist of a set of 
     optional behaviors that <b>LoadLibraryEx</b> provides:

<ul>
<li><b>LoadLibraryEx</b> can load a DLL module without 
      calling the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function of the DLL.</li>
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
     <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>.

The calling process can use the handle returned by 
    <b>LoadLibraryEx</b> to identify the module in calls to the 
    <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>, 
    <a href="https://msdn.microsoft.com/en-us/library/ms648042(v=VS.85).aspx">FindResource</a>, and 
    <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a> functions.

To enable or disable error messages displayed by the loader during DLL loads, use the 
    <a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a> function.

It is not safe to call <b>LoadLibraryEx</b> from 
    <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>. For more information, see the Remarks section in 
    <b>DllMain</b>.

<b>Visual C++:  </b>The Visual C++ compiler supports a syntax that enables you to declare thread-local variables: 
      <b>_declspec(thread)</b>. If you use this syntax in a DLL, you will not be able to load the 
      DLL explicitly using <b>LoadLibraryEx</b> on versions of 
      Windows prior to Windows Vista. If your DLL will be loaded explicitly, you must use the thread 
      local storage functions instead of <b>_declspec(thread)</b>. For an example, see 
      <a href="https://msdn.microsoft.com/a300f223-b513-4a22-a7a4-5d98cf74d77d">Using Thread Local Storage in a Dynamic Link Library</a>.

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
      image file but does not increment the reference count for the module and does not make the module visible to functions such as <a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> or <a href="https://msdn.microsoft.com/b4088506-2f69-4cf0-9bab-3e6a7185f5b2">EnumProcessModules</a>.

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
      <a href="https://msdn.microsoft.com/en-us/library/ms648042(v=VS.85).aspx">FindResource</a> can use either mapping.



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
 



Use the <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> function to free a loaded module, 
      whether or not loading the module caused its reference count to be incremented. If the module was loaded as a 
      data or image file, the mapping is destroyed but the reference count is not decremented. Otherwise, the DLL 
      reference count is decremented. Therefore, it is safe to call 
      <b>FreeLibrary</b> with any handle returned by 
      <b>LoadLibraryEx</b>.

<h3><a id="Searching_for_DLLs_and_Dependencies"></a><a id="searching_for_dlls_and_dependencies"></a><a id="SEARCHING_FOR_DLLS_AND_DEPENDENCIES"></a>Searching for DLLs and Dependencies</h3>
The search path is the set of directories that are searched for a DLL. The 
      <b>LoadLibraryEx</b> function can search for a DLL using a 
      standard search path or an altered search path, or it can use a process-specific search path established with 
      the <a href="https://msdn.microsoft.com/66884797-b1c8-4e50-aef1-e88944766d50">SetDefaultDllDirectories</a> and 
      <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> functions. For a list of directories 
      and the order in which they are searched, see 
      <a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>.

The <b>LoadLibraryEx</b> function uses the standard search 
      path in the following cases:
      <ul>
<li>The file name is specified without a path and the base file name does not match the base file name of a 
        loaded module, and none of the <b>LOAD_LIBRARY_SEARCH</b> flags are used.</li>
<li>A path is specified but <b>LOAD_WITH_ALTERED_SEARCH_PATH</b> is not used.</li>
<li>The application has not specified a default DLL search path for the process using 
        <a href="https://msdn.microsoft.com/66884797-b1c8-4e50-aef1-e88944766d50">SetDefaultDllDirectories</a>.</li>
</ul>


If <i>lpFileName</i> specifies a relative path, the entire relative path is appended to 
      every token in the DLL search path. To load a module from a relative path without searching any other path, use 
      <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a> to get a nonrelative path and call 
      <b>LoadLibraryEx</b> with the nonrelative path. If the module 
      is being loaded as a datafile and the relative path starts with  ".\" or 
      "..\", the relative path is treated as an absolute path.

If <i>lpFileName</i> specifies an absolute path and <i>dwFlags</i> is 
      set to <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>, 
      <b>LoadLibraryEx</b> uses the altered search path. 
      The behavior is undefined when <b>LOAD_WITH_ALTERED_SEARCH_PATH</b>flag is set, and <i>lpFileName</i> specifiies a relative path.

The <a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a> function can be used to modify 
      the search path. This solution is better than using 
      <a href="https://msdn.microsoft.com/en-us/library/Aa365530(v=VS.85).aspx">SetCurrentDirectory</a> or hard-coding the full path 
      to the DLL. However, be aware that using 
      <b>SetDllDirectory</b> effectively disables safe DLL search 
      mode while the specified directory is in the search path and it is not thread safe. If possible, it is best to 
      use <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> to modify a default process 
      search path. For more information, see 
      <a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>.

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
        <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> function 
        (<b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>) or the 
        <a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a> function. If more than one path 
        has been added, the  order in which the paths are searched is unspecified.</li>
<li>The System32 directory (<b>LOAD_LIBRARY_SEARCH_SYSTEM32</b>).</li>
</ul>


<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>The <b>LOAD_LIBRARY_SEARCH_*</b> flags are available on systems that have 
       <a href="Http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> 
       installed. To determine whether the flags are available, use 
       <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to get the address of the 
       <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a>, 
       <a href="https://msdn.microsoft.com/89ab63be-f0db-4f0f-9792-6976d867524e">RemoveDllDirectory</a>, or 
       <a href="https://msdn.microsoft.com/66884797-b1c8-4e50-aef1-e88944766d50">SetDefaultDllDirectories</a> function. If 
       <b>GetProcAddress</b> succeeds, the 
       <b>LOAD_LIBRARY_SEARCH_*</b> flags can be used with 
       <b>LoadLibraryEx</b>.

If the application has used the 
      <a href="https://msdn.microsoft.com/66884797-b1c8-4e50-aef1-e88944766d50">SetDefaultDllDirectories</a> function to 
      establish a DLL search path for the process and none of the <b>LOAD_LIBRARY_SEARCH_*</b> 
      flags are used, the <b>LoadLibraryEx</b> function uses the 
      process DLL search path instead of the standard search path.

If a path is specified and there is a redirection file associated with the application, the 
      <b>LoadLibraryEx</b> function searches for the module in the 
      application directory. If the module exists in the application directory, 
      <b>LoadLibraryEx</b> ignores the path specification and 
      loads the module from the application directory. If the module does not exist in the application directory, the 
      function loads the module from the specified directory. For more information, see 
      <a href="https://msdn.microsoft.com/3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8">Dynamic Link Library Redirection</a>.

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

Do not use the <a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> function to retrieve a path to 
      a DLL for a subsequent <b>LoadLibraryEx</b> call. The 
      <b>SearchPath</b> function uses a different search order than 
      <b>LoadLibraryEx</b> and it does not use safe process search 
      mode unless this is explicitly enabled by calling 
      <a href="https://msdn.microsoft.com/1874933d-92c3-4945-a3e4-e6dede232d5e">SetSearchPathMode</a> with 
      <b>BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE</b>. Therefore, 
      <b>SearchPath</b> is likely to first search the user’s current 
      working directory for the specified DLL. If an attacker has copied a malicious version of a DLL into the 
      current working directory, the path retrieved by 
      <b>SearchPath</b> will point to the malicious DLL, which 
      <b>LoadLibraryEx</b> will then load.

Do not make assumptions about the operating system version based on a 
      <b>LoadLibraryEx</b> call that searches for a DLL. If the 
      application is running in an environment where the DLL is legitimately not present but a malicious version of 
      the DLL is in the search path, the malicious version of the DLL may be loaded. Instead, use the recommended 
      techniques described in 
      <a href="https://msdn.microsoft.com/ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a">Getting the System Version</a>.

For a general discussion of DLL security issues, see 
      <a href="https://msdn.microsoft.com/9493F299-789D-4CBC-9822-96EEAE39B494">Dynamic-Link Library Security</a>.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/90ed87ca-7a08-4a66-b06a-e1bf668fb81a">Looking Up Text for Error Code Numbers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>



<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>



<a href="https://msdn.microsoft.com/9493F299-789D-4CBC-9822-96EEAE39B494">Dynamic-Link Library Security</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648042(v=VS.85).aspx">FindResource</a>



<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>



<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a>



<a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>
 

 

