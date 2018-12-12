---
UID: NF:processthreadsapi.CreateProcessAsUserA
title: CreateProcessAsUserA function
author: windows-sdk-content
description: Creates a new process and its primary thread. The new process runs in the security context of the user represented by the specified token.
old-location: base\createprocessasuser.htm
tech.root: procthread
ms.assetid: 6b3f4dd9-500b-420e-804a-401a9e188be8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateProcessAsUser, CreateProcessAsUser function, CreateProcessAsUserA, CreateProcessAsUserW, _win32_createprocessasuser, base.createprocessasuser, processthreadsapi/CreateProcessAsUser, processthreadsapi/CreateProcessAsUserA, processthreadsapi/CreateProcessAsUserW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateProcessAsUserW (Unicode) and CreateProcessAsUserA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Processsecurity-l1-1-0.dll
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-Processthreads-l1-1-0.dll
 - API-MS-Win-Core-Processthreads-l1-1-1.dll
 - API-MS-Win-Core-Processthreads-l1-1-2.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - CreateProcessAsUser
 - CreateProcessAsUserA
 - CreateProcessAsUserW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateProcessAsUserA function


## -description


Creates a new process and its primary thread. The new process runs in the security context of the user represented by the specified token.

Typically, the process that calls the 
<b>CreateProcessAsUser</b> function must have the <b>SE_INCREASE_QUOTA_NAME</b> privilege and may require the <b>SE_ASSIGNPRIMARYTOKEN_NAME</b> privilege if the token is  not assignable. If this function fails with <b>ERROR_PRIVILEGE_NOT_HELD</b> (1314), use the <a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a> function instead. <b>CreateProcessWithLogonW</b> requires no special privileges, but the specified user account must be allowed to log on interactively. Generally, it is best to use <b>CreateProcessWithLogonW</b> to create a process with alternate credentials.


## -parameters




### -param hToken [in, optional]

A handle to the primary token that represents a user. The handle must have the <b>TOKEN_QUERY</b>, <b>TOKEN_DUPLICATE</b>, and <b>TOKEN_ASSIGN_PRIMARY</b> access rights. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>. The user represented by the token must have read and execute access to the application specified by the <i>lpApplicationName</i> or the <i>lpCommandLine</i> parameter. 




To get a primary token that represents the specified user, call the 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function. Alternatively, you can call the 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a> function to convert an impersonation token into a primary token. This allows a server application that is impersonating a client to create a process that has the security context of the client.

If <i>hToken</i> is a restricted version of the caller's primary token, the <b>SE_ASSIGNPRIMARYTOKEN_NAME</b> privilege is not required. If the necessary privileges are not already enabled, 
<b>CreateProcessAsUser</b> enables them for the duration of the call. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

<b>Terminal Services:  </b>The process is run in the session specified in the token. By default, this is the same session that called <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>. To change the session, use the 
<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a> function.


### -param lpApplicationName [in, optional]

The name of the module to be executed. This module can be a Windows-based application. It can be some other type of module (for example, MS-DOS or OS/2) if the appropriate subsystem is available on the local computer. 




The string can specify the full path and file name of the module to execute or it can specify a partial name. In the case of a partial name, the function uses the current drive and current directory to complete the specification. The function will not use the search path. This parameter must include the file name extension; no default extension is assumed.

The <i>lpApplicationName</i> parameter can be <b>NULL</b>. In that case, the module name must be the first white space–delimited token in the <i>lpCommandLine</i> string. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin; otherwise, the file name is ambiguous. For example, consider the string "c:\program files\sub dir\program name". This string can be interpreted in a number of ways. The system tries to interpret the possibilities in the following order:

<b>c:\program.exe</b>
<b>c:\program files\sub.exe</b>
<b>c:\program files\sub dir\program.exe</b>
<b>c:\program files\sub dir\program name.exe</b>
If the executable module is a 16-bit application, <i>lpApplicationName</i> should be <b>NULL</b>, and the string pointed to by <i>lpCommandLine</i> should specify the executable module as well as its arguments. By default, all 16-bit Windows-based applications created by 
<b>CreateProcessAsUser</b> are run in a separate VDM (equivalent to <b>CREATE_SEPARATE_WOW_VDM</b> in 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>).


### -param lpCommandLine [in, out, optional]

The command line to be executed. The maximum length of this string is 32K characters. If <i>lpApplicationName</i> is <b>NULL</b>, the module name portion of <i>lpCommandLine</i> is limited to <b>MAX_PATH</b> characters.

The Unicode version of this function, <b>CreateProcessAsUserW</b>, can modify the contents of this string. Therefore, this parameter cannot be a pointer to read-only memory (such as a <b>const</b> variable or a literal string). If this parameter is a constant string, the function may cause an access violation.

The <i>lpCommandLine</i> parameter can be <b>NULL</b>. In that case, the function uses the string pointed to by <i>lpApplicationName</i> as the command line.

If both <i>lpApplicationName</i> and <i>lpCommandLine</i> are non-<b>NULL</b>, *<i>lpApplicationName</i> specifies the module to execute, and *<i>lpCommandLine</i> specifies the command line. The new process can use 
<a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine</a> to retrieve the entire command line. Console processes written in C can use the <i>argc</i> and <i>argv</i> arguments to parse the command line. Because <i>argv</i>[0] is the module name, C programmers generally repeat the module name as the first token in the command line.

If <i>lpApplicationName</i> is <b>NULL</b>, the first white space–delimited token of the command line specifies the module name. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin (see the explanation for the <i>lpApplicationName</i> parameter). If the file name does not contain an extension, .exe is appended. Therefore, if the file name extension is .com, this parameter must include the .com extension. If the file name ends in a period (.) with no extension, or if the file name contains a path, .exe is not appended. If the file name does not contain a directory path, the system searches for the executable file in the following sequence:

<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory for the parent process.</li>
<li>The 32-bit Windows system directory. Use the <a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a> function to get the path of this directory. </li>
<li>The 16-bit Windows system directory. There is no function that obtains the path of this directory, but it is searched. </li>
<li>The Windows directory. Use the 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable. Note that this function does not search the per-application path specified by the <b>App Paths</b> registry key. To include this per-application path in the search sequence, use the <a href="https://msdn.microsoft.com/en-us/library/Hh449546(v=VS.85).aspx">ShellExecute</a> function.</li>
</ol>
The system adds a null character to the command line string to separate the file name from the arguments. This divides the original string into two strings for internal processing.


### -param lpProcessAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new process object and determines whether child processes can inherit the returned handle to the process. If <i>lpProcessAttributes</i> is <b>NULL</b> or <b>lpSecurityDescriptor</b> is <b>NULL</b>, the process gets a default security descriptor and the handle cannot be inherited. The default security descriptor is that of the user referenced in the <i>hToken</i> parameter. This security descriptor may not allow access for the caller, in which case the process may not be opened again after it is run. The process handle is valid and will continue to have full access rights.


### -param lpThreadAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new thread object and determines whether child processes can inherit the returned handle to the thread. If <i>lpThreadAttributes</i> is <b>NULL</b> or <b>lpSecurityDescriptor</b> is <b>NULL</b>, the thread gets a default security descriptor and the handle cannot be inherited. The default security descriptor is that of the user referenced in the <i>hToken</i> parameter. This security descriptor may not allow access for the caller.


### -param bInheritHandles [in]

If this parameter is <b>TRUE</b>, each inheritable handle in the calling process is inherited by the new process. If the parameter is <b>FALSE</b>, the handles are not inherited. Note that inherited handles have the same value and access rights as the original handles.


<b>Terminal Services:  </b>You cannot inherit handles across sessions. Additionally, if this parameter is <b>TRUE</b>, you must create the process in the same session as the caller.

<b>Protected Process Light (PPL) processes:  </b>The generic handle inheritance is blocked when a PPL process creates a non-PPL process since PROCESS_DUP_HANDLE is not allowed from a non-PPL process to a PPL process. See <a href="https://msdn.microsoft.com/library/windows/desktop/ms684880.aspx">Process Security and Access Rights</a>


### -param dwCreationFlags [in]

The flags that control the priority class and the creation of the process. For a list of values, see 
<a href="https://msdn.microsoft.com/fd3384ad-8635-4ea1-9054-0572ef86b86d">Process Creation Flags</a>. 




This parameter also controls the new process's priority class, which is used to determine the scheduling priorities of the process's threads. For a list of values, see 
<a href="https://msdn.microsoft.com/2a16b18f-8efa-43f0-9f7d-d38cc8a153d3">GetPriorityClass</a>. If none of the priority class flags is specified, the priority class defaults to <b>NORMAL_PRIORITY_CLASS</b> unless the priority class of the creating process is <b>IDLE_PRIORITY_CLASS</b> or <b>BELOW_NORMAL_PRIORITY_CLASS</b>. In this case, the child process receives the default priority class of the calling process.


### -param lpEnvironment [in, optional]

A pointer to an environment block for the new process. If this parameter is <b>NULL</b>, the new process uses the environment of the calling process. 




An environment block consists of a null-terminated block of null-terminated strings. Each string is in the following form:

<i>name</i>=<i>value</i>\0

Because the equal sign is used as a separator, it must not be used in the name of an environment variable.

An environment block can contain either Unicode or ANSI characters. If the environment block pointed to by <i>lpEnvironment</i> contains Unicode characters, be sure that <i>dwCreationFlags</i> includes <b>CREATE_UNICODE_ENVIRONMENT</b>.  If this parameter is <b>NULL</b> and the environment block of the parent process contains Unicode characters, you must also ensure that <i>dwCreationFlags</i> includes <b>CREATE_UNICODE_ENVIRONMENT</b>.

The ANSI version of this function, <b>CreateProcessAsUserA</b> fails if the total size of the environment block for the process exceeds 32,767 characters.

Note that an ANSI environment block is terminated by two zero bytes: one for the last string, one more to terminate the block. A Unicode environment block is terminated by four zero bytes: two for the last string, two more to terminate the block.

<b>Windows Server 2003 and Windows XP:  </b>If the size of the combined user and system environment variable exceeds 8192 bytes, the process created by <b>CreateProcessAsUser</b> no longer runs with the environment block passed to the function by the parent process. Instead, the child process runs with the environment block returned by the <a href="https://msdn.microsoft.com/bda8879d-d33a-48f4-8b08-e3a279126a07">CreateEnvironmentBlock</a> function.



To retrieve a copy of the environment block for a given user, use the 
<a href="https://msdn.microsoft.com/en-us/library/Bb762270(v=VS.85).aspx">CreateEnvironmentBlock</a> function.


### -param lpCurrentDirectory [in, optional]

The full path to the current directory for the process. The string can also specify a UNC path. 

If this parameter is NULL, the new process will have the same current drive and directory as the calling process. (This feature is provided primarily for shells that need to start an application and specify its initial drive and working directory.)


### -param lpStartupInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure.

The user must have full access to both the specified window station and desktop. If you want the process to be interactive, specify winsta0\default. If the <b>lpDesktop</b> member is NULL, the new process inherits the desktop and window station of its parent process. 
If this member is an empty string, "", the new process connects to a window station using the rules described in <a href="https://msdn.microsoft.com/280f69e7-5c99-41a7-94e3-da13deaac9f5">Process Connection to a Window Station</a>.

To set extended attributes, use a <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure and specify <b>EXTENDED_STARTUPINFO_PRESENT</b> in the <i>dwCreationFlags</i> parameter.

Handles in 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> must be closed with 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when they are no longer needed.

<div class="alert"><b>Important</b>  The caller is responsible for ensuring that the standard handle fields in <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> contain valid handle values. These fields are copied unchanged to the child process without validation, even when the <b>dwFlags</b> member specifies <b>STARTF_USESTDHANDLES</b>. Incorrect values can cause the child process to misbehave or crash. Use the <a href="http://go.microsoft.com/fwlink/p/?linkid=234779">Application Verifier</a> runtime verification tool to detect invalid handles. </div>
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



<b>CreateProcessAsUser</b> must be able to open the primary token of the calling process with the <b>TOKEN_DUPLICATE</b> and <b>TOKEN_IMPERSONATE</b> access rights.

By default, 
<b>CreateProcessAsUser</b> creates the new process on a noninteractive window station with a desktop that is not visible and cannot receive user input. To enable user interaction with the new process, you must specify the name of the default interactive window station and desktop, "winsta0\default", in the <b>lpDesktop</b> member of the 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure. In addition, before calling 
<b>CreateProcessAsUser</b>, you must change the discretionary access control list (DACL) of both the default interactive window station and the default desktop. The DACLs for the window station and desktop must grant access to the user or the logon session represented by the <i>hToken</i> parameter.

<b>CreateProcessAsUser</b> does not load the specified user's profile into the <b>HKEY_USERS</b> registry key. Therefore, to access the information in the <b>HKEY_CURRENT_USER</b> registry key, you must load the user's profile information into <b>HKEY_USERS</b> with the 
<a href="https://msdn.microsoft.com/en-us/library/Bb762281(v=VS.85).aspx">LoadUserProfile</a> function before calling 
<b>CreateProcessAsUser</b>. Be sure to call <a href="https://msdn.microsoft.com/en-us/library/Bb762282(v=VS.85).aspx">UnloadUserProfile</a> after the new process exits.

If the <i>lpEnvironment</i> parameter is NULL, the new process inherits the environment of the calling process. 
<b>CreateProcessAsUser</b> does not automatically modify the environment block to include environment variables specific to the user represented by <i>hToken</i>. For example, the USERNAME and USERDOMAIN variables are inherited from the calling process if <i>lpEnvironment</i> is NULL. It is your responsibility to prepare the environment block for the new process and specify it in <i>lpEnvironment</i>.

The 
<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>    and <a href="https://msdn.microsoft.com/b329866a-0c0d-4cb3-838c-36aac17c87ed">CreateProcessWithTokenW</a> functions are similar to 
<b>CreateProcessAsUser</b>, except that the caller does not need to call the 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function to authenticate the user and get a token.

<b>CreateProcessAsUser</b> allows you to access the specified directory and executable image in the security context of the caller or the target user. By default, 
<b>CreateProcessAsUser</b> accesses the directory and executable image in the security context of the caller. In this case, if the caller does not have access to the directory and executable image, the function fails. To access the directory and executable image using the security context of the target user, specify <i>hToken</i> in a call to the 
<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> function before calling 
<b>CreateProcessAsUser</b>.

The process is assigned a process identifier. The identifier is valid until the process terminates. It can be used to identify the process, or specified in the 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function to open a handle to the process. The initial thread in the process is also assigned a thread identifier. It can be specified in the 
<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function to open a handle to the thread. The identifier is valid until the thread terminates and can be used to uniquely identify the thread within the system. These identifiers are returned in the 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure.

The calling thread can use the 
<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> function to wait until the new process has finished its initialization and is waiting for user input with no input pending. This can be useful for synchronization between parent and child processes, because 
<b>CreateProcessAsUser</b> returns without waiting for the new process to finish its initialization. For example, the creating process would use 
<b>WaitForInputIdle</b> before trying to find a window associated with the new process.

The preferred way to shut down a process is by using the 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> function, because this function sends notification of approaching termination to all DLLs attached to the process. Other means of shutting down a process do not notify the attached DLLs. Note that when a thread calls 
<b>ExitProcess</b>, other threads of the process are terminated without an opportunity to execute any additional code (including the thread termination code of attached DLLs). For more information, see 
<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The <i>lpApplicationName</i> parameter can be NULL, in which case the executable name must be the first white space–delimited string in <i>lpCommandLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. The following example is dangerous because the function will attempt to run "Program.exe", if it exists, instead of "MyApp.exe".

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline[] = _tcsdup(TEXT("C:\\Program Files\\MyApp"));
	CreateProcessAsUser(hToken, NULL, szCmdline, /*...*/ );</code></pre>
If a malicious user were to create an application called "Program.exe" on a system, any program that incorrectly calls 
<b>CreateProcessAsUser</b> using the Program Files directory will run this application instead of the intended application.

To avoid this problem, do not pass NULL for <i>lpApplicationName</i>. If you do pass <b>NULL</b> for <i>lpApplicationName</i>, use quotation marks around the executable path in <i>lpCommandLine</i>, as shown in the example below.

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline[] = _tcsdup(TEXT("\"C:\\Program Files\\MyApp\""));
	CreateProcessAsUser(hToken, NULL, szCmdline, /*...*/);</code></pre>
<b>PowerShell:  </b>When the <b>CreateProcessAsUser</b> function is used to implement a cmdlet in PowerShell version 2.0, the cmdlet operates correctly for both fan-in and fan-out remote sessions. Because of certain security scenarios, however, a cmdlet implemented with <b>CreateProcessAsUser</b> only operates correctly in PowerShell version 3.0 for fan-in remote sessions; fan-out remote sessions will fail because of insufficient client security privileges. To implement a cmdlet that works for both fan-in and fan-out remote sessions in PowerShell version 3.0, use the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/library/Aa379608(v=VS.85).aspx">Starting an Interactive Client Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762270(v=VS.85).aspx">CreateEnvironmentBlock</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683230(v=VS.85).aspx">GetStartupInfo</a>



<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762281(v=VS.85).aspx">LoadUserProfile</a>



<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762138(v=VS.85).aspx">SHCreateProcessAsUserW</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>



<a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a>
 

 

