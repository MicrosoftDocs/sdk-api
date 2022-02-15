---
UID: NF:winbase.LoadModule
title: LoadModule function (winbase.h)
description: Loads and executes an application or creates a new instance of an existing application.
helpviewer_keywords: ["LOADPARMS32","LoadModule","LoadModule function","_win32_loadmodule","base.loadmodule","winbase/LoadModule"]
old-location: base\loadmodule.htm
tech.root: base
ms.assetid: 80571b80-851a-4272-bfa6-d26e217e714a
ms.date: 12/05/2018
ms.keywords: LOADPARMS32, LoadModule, LoadModule function, _win32_loadmodule, base.loadmodule, winbase/LoadModule
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadModule
 - winbase/LoadModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - LoadModule
---

# LoadModule function


## -description

Loads and executes an application or creates a new instance of an existing application.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function.</div><div> </div>

## -parameters

### -param lpModuleName [in]

The file name of the application to be run. When specifying a path, be sure to use backslashes (\\), not forward slashes (/). If the <i>lpModuleName</i> parameter does not contain a directory path, the system searches for the executable file in this order: 




<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory.</li>
<li>The system directory. Use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a> function to get the path of this directory. 


</li>
<li> The 16-bit system directory. There is no function that obtains the path of this directory, but it is searched. The name of this directory is System.</li>
<li>The Windows directory. Use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable.</li>
</ol>

### -param lpParameterBlock [in]

A pointer to an application-defined <b>LOADPARMS32</b> structure that defines the new application's parameter block. 


Set all unused members to NULL, except for <b>lpCmdLine</b>, which must point to a null-terminated string if it is not used. For more information, see Remarks.

## -returns

If the function succeeds, the return value is greater than 31.

If the function fails, the return value is an error value, which may be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system is out of memory or resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
<dt>11L</dt>
</dl>
</td>
<td width="60%">
The .exe file is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
The specified file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
<dt>3L</dt>
</dl>
</td>
<td width="60%">
The specified path was not found.

</td>
</tr>
</table>

## -remarks

The <b>LOADPARMS32</b> structure has the following form:
						


``` syntax
typedef struct tagLOADPARMS32 { 
  LPSTR lpEnvAddress;  // address of environment strings 
  LPSTR lpCmdLine;     // address of command line 
  LPSTR lpCmdShow;     // how to show new program 
  DWORD dwReserved;    // must be zero 
} LOADPARMS32;
```

<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>lpEnvAddress</b></td>
<td>Pointer to an array of null-terminated strings that supply the environment strings for the new process. The array has a value of NULL as its last entry. A value of NULL for this parameter causes the new process to start with the same environment as the calling process.</td>
</tr>
<tr>
<td><b>lpCmdLine</b></td>
<td>Pointer to a Pascal-style string that contains a correctly formed command line. The first byte of the string contains the number of bytes in the string. The remainder of the string contains the command line arguments, excluding the name of the child process. If there are no command line arguments, this parameter must point to a zero length string; it cannot be NULL.</td>
</tr>
<tr>
<td><b>lpCmdShow</b></td>
<td>Pointer to a structure containing two <b>WORD</b> values. The first value must always be set to two. The second value specifies how the application window is to be shown and is used to supply the <b>wShowWindow</b> member of the 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function. See the description of the <i>nCmdShow</i> parameter of the 
<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function for a list of acceptable values.</td>
</tr>
<tr>
<td><b>dwReserved</b></td>
<td>This parameter is reserved; it must be zero.</td>
</tr>
</table>
 

Applications should use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function instead of 
<b>LoadModule</b>. The 
<b>LoadModule</b> function calls 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> by forming the parameters as follows.
				

<table>
<tr>
<th>CreateProcess parameter</th>
<th>Argument used</th>
</tr>
<tr>
<td><i>lpszApplicationName</i></td>
<td><i>lpModuleName</i></td>
</tr>
<tr>
<td><i>lpszCommandLine</i></td>
<td><i>lpParameterBlock</i>.<b>lpCmdLine</b></td>
</tr>
<tr>
<td><i>lpProcessAttributes</i></td>
<td>NULL</td>
</tr>
<tr>
<td><i>lpThreadAttributes</i></td>
<td>NULL</td>
</tr>
<tr>
<td><i>bInheritHandles</i></td>
<td>FALSE</td>
</tr>
<tr>
<td><i>dwCreationFlags</i></td>
<td>0</td>
</tr>
<tr>
<td><i>lpEnvironment</i></td>
<td><i>lpParameterBlock</i>.<b>lpEnvAddress</b></td>
</tr>
<tr>
<td><i>lpCurrentDirectory</i></td>
<td>NULL</td>
</tr>
<tr>
<td><i>lpStartupInfo</i></td>
<td>The structure is initialized to zero. The <b>cb</b> member is set to the size of the structure. The <b>wShowWindow</b> member is set to the value of the second word of <i>lpParameterBlock</i>.<b>lpCmdShow</b>.</td>
</tr>
<tr>
<td><i>lpProcessInformation</i><b>.hProcess</b></td>
<td>The handle is immediately closed.</td>
</tr>
<tr>
<td><i>lpProcessInformation</i><b>.hThread</b></td>
<td>The handle is immediately closed.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>
