---
UID: NF:processthreadsapi.CreateProcessA
title: CreateProcessA function
author: windows-sdk-content
description: Creates a new process and its primary thread. The new process runs in the security context of the calling process.
old-location: base\createprocess.htm
tech.root: procthread
ms.assetid: 3ef0a5b2-4d71-4c17-8188-76a4025287fc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateProcess, CreateProcess function, CreateProcessA, CreateProcessW, _win32_createprocess, base.createprocess, processthreadsapi/CreateProcess, processthreadsapi/CreateProcessA, processthreadsapi/CreateProcessW, winbase/CreateProcess, winbase/CreateProcessA, winbase/CreateProcessW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateProcessW (Unicode) and CreateProcessA (ANSI)
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - CreateProcess
 - CreateProcessA
 - CreateProcessW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateProcessA
: 
---

# CreateProcessA function


## -description


Creates a new process and its primary thread. The new process runs in the security context of the calling process.

If the calling process is impersonating another user, the new process uses the token for the calling process, not the impersonation token. To run the new process in the security context of the user represented by the impersonation token, use the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> or 
<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a> function.


## -parameters




### -param lpApplicationName [in, optional]

The name of the module to be executed. This module can be a Windows-based application. It can be some other type of module (for example, MS-DOS or OS/2) if the appropriate subsystem is available on the local computer. 




The string can specify the full path and file name of the module to execute or it can specify a partial name. In the case of a partial name, the function uses the current drive and current directory to complete the specification. The function will not use the search path. This parameter must include the file name extension; no default extension is assumed.

The <i>lpApplicationName</i> parameter can be <b>NULL</b>. In that case, the module name must be the first white space–delimited token in the <i>lpCommandLine</i> string. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin; otherwise, the file name is ambiguous. For example, consider the string "c:\program files\sub dir\program name". This string can be interpreted in a number of ways. The system tries to interpret the possibilities in the following order:

<b>c:\program.exe</b>
<b>c:\program files\sub.exe</b>
<b>c:\program files\sub dir\program.exe</b>
<b>c:\program files\sub dir\program name.exe</b>
If the executable module is a 16-bit application, <i>lpApplicationName</i> should be <b>NULL</b>, and the string pointed to by <i>lpCommandLine</i> should specify the executable module as well as its arguments.

To run a batch file, you must start the command interpreter; set <i>lpApplicationName</i> to cmd.exe and set <i>lpCommandLine</i> to the following arguments: /c plus the name of the batch file.


### -param lpCommandLine [in, out, optional]

The command line to be executed. 


The maximum length of this string is 32,768 characters, including the Unicode terminating null character. If <i>lpApplicationName</i> is <b>NULL</b>, the module name portion of <i>lpCommandLine</i> is limited to <b>MAX_PATH</b> characters.

The Unicode version of this function, <b>CreateProcessW</b>, can modify the contents of this string. Therefore, this parameter cannot be a pointer to read-only memory (such as a <b>const</b> variable or a literal string). If this parameter is a constant string, the function may cause an access violation.

The <i>lpCommandLine</i> parameter can be NULL. In that case, the function uses the string pointed to by <i>lpApplicationName</i> as the command line.

If both <i>lpApplicationName</i> and <i>lpCommandLine</i> are non-<b>NULL</b>,  the null-terminated string pointed to by <i>lpApplicationName</i> specifies the module to execute, and the null-terminated string pointed to by  <i>lpCommandLine</i> specifies the command line. The new process can use 
<a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine</a> to retrieve the entire command line. Console processes written in C can use the <i>argc</i> and <i>argv</i> arguments to parse the command line. Because argv[0] is the module name, C programmers generally repeat the module name as the first token in the command line.

If <i>lpApplicationName</i> is NULL, the first white space–delimited token of the command line specifies the module name. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin (see the explanation for the <i>lpApplicationName</i> parameter). If the file name does not contain an extension, .exe is appended. Therefore, if the file name extension is .com, this parameter must include the .com extension. If the file name ends in a period (.) with no extension, or if the file name contains a path, .exe is not appended. If the file name does not contain a directory path, the system searches for the executable file in the following sequence:

<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory for the parent process.</li>
<li>The 32-bit Windows system directory. Use the <a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a> function to get the path of this directory.</li>
<li> The 16-bit Windows system directory. There is no function that obtains the path of this directory, but it is searched. The name of this directory is System.</li>
<li>The Windows directory. Use the 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable. Note that this function does not search the per-application path specified by the <b>App Paths</b> registry key. To include this per-application path in the search sequence, use the <a href="_win32_ShellExecute_cpp">ShellExecute</a> function.</li>
</ol>
The system adds a terminating null character to the command-line string to separate the file name from the arguments. This divides the original string into two strings for internal processing.


### -param lpProcessAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle to the new process object can be inherited by child processes. If <i>lpProcessAttributes</i> is <b>NULL</b>, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new process. If <i>lpProcessAttributes</i> is NULL or <b>lpSecurityDescriptor</b> is <b>NULL</b>, the process gets a default security descriptor. The ACLs in the default security descriptor for a process come from the primary token of the creator.<b>Windows XP:  </b>The ACLs in the default security descriptor for a process come from the primary or impersonation token of the creator. This behavior changed with Windows XP with SP2 and Windows Server 2003.




### -param lpThreadAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle to the new thread object can be inherited by child processes. If <i>lpThreadAttributes</i> is NULL, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the main thread. If <i>lpThreadAttributes</i> is NULL or <b>lpSecurityDescriptor</b> is NULL, the thread gets a default security descriptor. The ACLs in the default security descriptor for a thread come from the process token.<b>Windows XP:  </b>The ACLs in the default security descriptor for a thread come from the primary or impersonation token of the creator. This behavior changed with Windows XP with SP2 and Windows Server 2003.




### -param bInheritHandles [in]

If this parameter is TRUE, each inheritable handle in the calling process is inherited by the new process. If the parameter is FALSE, the handles are not inherited. Note that inherited handles have the same value and access rights as the original handles.

<b>Terminal Services:  </b>You cannot inherit handles across sessions. Additionally, if this parameter is TRUE, you must create the process in the same session as the caller.

<b>Protected Process Light (PPL) processes:  </b>The generic handle inheritance is blocked when a PPL process creates a non-PPL process since PROCESS_DUP_HANDLE is not allowed from a non-PPL process to a PPL process. See <a href="https://msdn.microsoft.com/library/windows/desktop/ms684880.aspx">Process Security and Access Rights</a>


### -param dwCreationFlags [in]

The flags that control the priority class and the creation of the process. For a list of values, see 
<a href="https://msdn.microsoft.com/fd3384ad-8635-4ea1-9054-0572ef86b86d">Process Creation Flags</a>. 




This parameter also controls the new process's priority class, which is used to determine the scheduling priorities of the process's threads. For a list of values, see 
<a href="https://msdn.microsoft.com/2a16b18f-8efa-43f0-9f7d-d38cc8a153d3">GetPriorityClass</a>. If none of the priority class flags is specified, the priority class defaults to <b>NORMAL_PRIORITY_CLASS</b> unless the priority class of the creating process is <b>IDLE_PRIORITY_CLASS</b> or <b>BELOW_NORMAL_PRIORITY_CLASS</b>. In this case, the child process receives the default priority class of the calling process.


### -param lpEnvironment [in, optional]

A pointer to the environment block for the new process. If this parameter is <b>NULL</b>, the new process uses the environment of the calling process.

An environment block consists of a null-terminated block of null-terminated strings. Each string is in the following form:

<i>name</i>=<i>value</i>\0

Because the equal sign is used as a separator, it must not be used in the name of an environment variable.

An environment block can contain either Unicode or ANSI characters. If the environment block pointed to by <i>lpEnvironment</i> contains Unicode characters, be sure that <i>dwCreationFlags</i> includes <b>CREATE_UNICODE_ENVIRONMENT</b>. If this parameter is <b>NULL</b> and the environment block of the parent process contains Unicode characters, you must also ensure that <i>dwCreationFlags</i> includes <b>CREATE_UNICODE_ENVIRONMENT</b>.

The ANSI version of this function, <b>CreateProcessA</b> fails if the total size of the environment block for the process exceeds 32,767 characters.

Note that an ANSI environment block is terminated by two zero bytes: one for the last string, one more to terminate the block. A Unicode environment block is terminated by four zero bytes: two for the last string, two more to terminate the block.


### -param lpCurrentDirectory [in, optional]

The full path to the current directory for the process. The string can also specify a UNC path.

If this parameter is <b>NULL</b>, the new process will have the same current drive and directory as the calling process. (This feature is provided primarily for shells that need to start an application and specify its initial drive and working directory.)


### -param lpStartupInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure.

To set extended attributes, use a <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure and specify EXTENDED_STARTUPINFO_PRESENT in the <i>dwCreationFlags</i> parameter.

Handles in 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> must be closed with 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when they are no longer needed.

<div class="alert"><b>Important</b>  The caller is responsible for ensuring that the standard handle fields in <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>  contain valid handle values. These fields are copied unchanged to the child process without validation, even when the <b>dwFlags</b> member specifies <b>STARTF_USESTDHANDLES</b>. Incorrect values can cause the child process to misbehave or crash. Use the <a href="http://go.microsoft.com/fwlink/p/?linkid=234779">Application Verifier</a> runtime verification tool to detect invalid handles. </div>
<div> </div>

### -param lpProcessInformation [out]

A pointer to a 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure that receives identification information about the new process. 




Handles in 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> must be closed with 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when they are no longer needed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Note that the function returns before the process has finished initialization. If a required DLL cannot be located or fails to initialize, the process is terminated. To get the termination status of a process, call <a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>. 




## -remarks



The process is assigned a process identifier. The identifier is valid until the process terminates. It can be used to identify the process, or specified in the 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function to open a handle to the process. The initial thread in the process is also assigned a thread identifier. It can be specified in the 
<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function to open a handle to the thread. The identifier is valid until the thread terminates and can be used to uniquely identify the thread within the system. These identifiers are returned in the 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure.

The name of the executable in the command line that the operating system provides to a process is not necessarily identical to that in the command line that the calling process gives to the 
<b>CreateProcess</b> function. The operating system may prepend a fully qualified path to an executable name that is provided without a fully qualified path.

The calling thread can use the 
<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> function to wait until the new process has finished its initialization and is waiting for user input with no input pending. This can be useful for synchronization between parent and child processes, because 
<b>CreateProcess</b> returns without waiting for the new process to finish its initialization. For example, the creating process would use 
<b>WaitForInputIdle</b> before trying to find a window associated with the new process.

The preferred way to shut down a process is by using the 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> function, because this function sends notification of approaching termination to all DLLs attached to the process. Other means of shutting down a process do not notify the attached DLLs. Note that when a thread calls 
<b>ExitProcess</b>, other threads of the process are terminated without an opportunity to execute any additional code (including the thread termination code of attached DLLs). For more information, see 
<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>.

A  parent process can directly alter the environment variables of a child process during process creation.  This is the only  situation when a process can directly change the environment settings of another process. For more information, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

If an application provides an environment block, the current directory information of the system drives is not automatically propagated to the new process. For example, there is an environment variable named =C: whose value is the current directory on drive C. An application must manually pass the current directory information to the new process. To do so, the application must explicitly create these environment variable strings, sort them alphabetically (because the system uses a sorted environment), and put them into the environment block. Typically, they will go at the front of the environment block, due to the environment block sort order.

One way to obtain the current directory information for a drive X is to make the following call: 
<code>GetFullPathName("X:", ...)</code>. That avoids an application having to scan the environment block. If the full path returned is X:\, there is no need to pass that value on as environment data, since the root directory is the default current directory for drive X of a new process.

When a process is created with <b>CREATE_NEW_PROCESS_GROUP</b> specified, an implicit call to 
<a href="base.setconsolectrlhandler">SetConsoleCtrlHandler</a>(<b>NULL</b>,<b>TRUE</b>) is made on behalf of the new process; this means that the new process has CTRL+C disabled. This lets shells handle CTRL+C themselves, and selectively pass that signal on to sub-processes. CTRL+BREAK is not disabled, and may be used to interrupt the process/process group.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The first parameter, <i>lpApplicationName</i>, can be <b>NULL</b>, in which case the executable name must be in the  white space–delimited string pointed to by <i>lpCommandLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. The following example is dangerous because the function will attempt to run "Program.exe", if it exists, instead of "MyApp.exe".

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline = _tcsdup(TEXT("C:\\Program Files\\MyApp -L -S"));
	CreateProcess(NULL, szCmdline, /* ... */);</code></pre>
If a malicious user were to create an application called "Program.exe" on a system, any program that incorrectly calls 
<b>CreateProcess</b> using the Program Files directory will run this application instead of the intended application.

To avoid this problem, do not pass <b>NULL</b> for <i>lpApplicationName</i>. If you do pass <b>NULL</b> for <i>lpApplicationName</i>, use quotation marks around the executable path in <i>lpCommandLine</i>, as shown in the example below.

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline[] = _tcsdup(TEXT("\"C:\\Program Files\\MyApp\" -L -S"));
	CreateProcess(NULL, szCmdline, /*...*/);</code></pre>

#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4">Creating Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine</a>



<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>



<a href="https://msdn.microsoft.com/191ea201-dc86-4cde-a0cd-be8d2360b22e">GetStartupInfo</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>



<a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>



<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a>
 

 

