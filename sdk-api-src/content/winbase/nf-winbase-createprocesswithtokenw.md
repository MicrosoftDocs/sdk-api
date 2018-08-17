---
UID: NF:winbase.CreateProcessWithTokenW
title: CreateProcessWithTokenW function
author: windows-sdk-content
description: Creates a new process and its primary thread. The new process runs in the security context of the specified token. It can optionally load the user profile for the specified user.
old-location: base\createprocesswithtokenw.htm
old-project: procthread
ms.assetid: b329866a-0c0d-4cb3-838c-36aac17c87ed
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: CREATE_DEFAULT_ERROR_MODE, CREATE_NEW_CONSOLE, CREATE_NEW_PROCESS_GROUP, CREATE_SEPARATE_WOW_VDM, CREATE_SUSPENDED, CREATE_UNICODE_ENVIRONMENT, CreateProcessWithTokenW, CreateProcessWithTokenW function, EXTENDED_STARTUPINFO_PRESENT, LOGON_NETCREDENTIALS_ONLY, LOGON_WITH_PROFILE, base.createprocesswithtokenw, winbase/CreateProcessWithTokenW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - AdvApi32Legacy.dll
 - API-MS-Win-Security-Cpwl-L1-1-0.dll
api_name:
 - CreateProcessWithTokenW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateProcessWithTokenW function


## -description


Creates a new process and its primary thread. The new process runs in the security context of the specified token. It can optionally load the user profile for the specified user.

The process that calls <b>CreateProcessWithTokenW</b> must have the SE_IMPERSONATE_NAME privilege. If this function fails with ERROR_PRIVILEGE_NOT_HELD (1314), use the <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> or <a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a> function instead. Typically, the process that calls  
<b>CreateProcessAsUser</b>  must have the SE_INCREASE_QUOTA_NAME privilege and may require the SE_ASSIGNPRIMARYTOKEN_NAME privilege if the token is  not assignable.    <b>CreateProcessWithLogonW</b> requires no special privileges, but the specified user account must be allowed to log on interactively. Generally, it is best to use <b>CreateProcessWithLogonW</b> to create a process with alternate credentials.


## -parameters




### -param hToken [in]

A handle to the primary token that represents a user. The handle must have the TOKEN_QUERY, TOKEN_DUPLICATE, and TOKEN_ASSIGN_PRIMARY access rights. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>. The user represented by the token must have read and execute access to the application specified by the <i>lpApplicationName</i> or the <i>lpCommandLine</i> parameter. 




To get a primary token that represents the specified user, call the 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function. Alternatively, you can call the 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a> function to convert an impersonation token into a primary token. This allows a server application that is impersonating a client to create a process that has the security context of the client.

<b>Terminal Services:  </b>The process is run in the session specified in the token. By default, this is the same session that called <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>. To change the session, use the 
<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a> function.


### -param dwLogonFlags [in]

The logon option. This parameter can be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_WITH_PROFILE"></a><a id="logon_with_profile"></a><dl>
<dt><b>LOGON_WITH_PROFILE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Log on, then load the user's profile in the <b>HKEY_USERS</b> registry key. The function returns after the profile has been loaded. Loading the profile can be time-consuming, so it is best to use this value only if you must access the information in the <b>HKEY_CURRENT_USER</b> registry key. 




<b>Windows Server 2003:  </b>The profile is unloaded after the new process has been terminated, regardless of whether it has created child processes.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_NETCREDENTIALS_ONLY"></a><a id="logon_netcredentials_only"></a><dl>
<dt><b>LOGON_NETCREDENTIALS_ONLY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Log on, but use the specified credentials on the network only. The new process uses the same token as the caller, but the system creates a new logon session within LSA, and the process uses the specified credentials as the default credentials. 




This value can be used to create a process that uses a different set of credentials locally than it does remotely. This is useful in inter-domain scenarios where there is no trust relationship.

The system does not validate the specified credentials. Therefore, the process can start, but it may not have access to network resources.

</td>
</tr>
</table>
 


### -param lpApplicationName [in, optional]

The name of the module to be executed. This module can be a Windows-based application. It can be some other type of module (for example, MS-DOS or OS/2) if the appropriate subsystem is available on the local computer. 




The string can specify the full path and file name of the module to execute or it can specify a partial name. In the case of a partial name, the function uses the current drive and current directory to complete the specification. The function will not use the search path. This parameter must include the file name extension; no default extension is assumed.

The <i>lpApplicationName</i> parameter can be NULL. In that case, the module name must be the first white space–delimited token in the <i>lpCommandLine</i> string. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin; otherwise, the file name is ambiguous. For example, consider the string "c:\program files\sub dir\program name". This string can be interpreted in a number of ways. The system tries to interpret the possibilities in the following order:

<b>c:\program.exe</b>
<b>c:\program files\sub.exe</b>
<b>c:\program files\sub dir\program.exe</b>
<b>c:\program files\sub dir\program name.exe</b>
If the executable module is a 16-bit application, <i>lpApplicationName</i> should be NULL, and the string pointed to by <i>lpCommandLine</i> should specify the executable module as well as its arguments.


### -param lpCommandLine [in, out, optional]

The command line to be executed. 


The maximum length of this string is 1024 characters. If <i>lpApplicationName</i> is NULL, the module name portion of <i>lpCommandLine</i> is limited to MAX_PATH characters.

The function can modify the contents of this string. Therefore, this parameter cannot be a pointer to read-only memory (such as a <b>const</b> variable or a literal string). If this parameter is a constant string, the function may cause an access violation.

The <i>lpCommandLine</i> parameter can be NULL. In that case, the function uses the string pointed to by <i>lpApplicationName</i> as the command line.

If both <i>lpApplicationName</i> and <i>lpCommandLine</i> are non-NULL, *<i>lpApplicationName</i> specifies the module to execute, and *<i>lpCommandLine</i> specifies the command line. The new process can use 
<a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine</a> to retrieve the entire command line. Console processes written in C can use the <i>argc</i> and <i>argv</i> arguments to parse the command line. Because argv[0] is the module name, C programmers generally repeat the module name as the first token in the command line.

If <i>lpApplicationName</i> is NULL, the first white space–delimited token of the command line specifies the module name. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin (see the explanation for the <i>lpApplicationName</i> parameter). If the file name does not contain an extension, .exe is appended. Therefore, if the file name extension is .com, this parameter must include the .com extension. If the file name ends in a period (.) with no extension, or if the file name contains a path, .exe is not appended. If the file name does not contain a directory path, the system searches for the executable file in the following sequence:

<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory for the parent process.</li>
<li>The 32-bit Windows system directory. Use the <a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a> function to get the path of this directory.</li>
<li>The 16-bit Windows system directory. There is no function that obtains the path of this directory, but it is searched.</li>
<li>The Windows directory. Use the 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable. Note that this function does not search the per-application path specified by the <b>App Paths</b> registry key. To include this per-application path in the search sequence, use the <a href="_win32_ShellExecute_cpp">ShellExecute</a> function.</li>
</ol>
The system adds a null character to the command line string to separate the file name from the arguments. This divides the original string into two strings for internal processing.


### -param dwCreationFlags [in]

The flags that control how the process is created. The CREATE_DEFAULT_ERROR_MODE, CREATE_NEW_CONSOLE, and CREATE_NEW_PROCESS_GROUP flags are enabled by default. You can specify additional flags as noted. 



                     
                     
                  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_DEFAULT_ERROR_MODE"></a><a id="create_default_error_mode"></a><dl>
<dt><b>CREATE_DEFAULT_ERROR_MODE</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The new process does not inherit the error mode of the calling process. Instead, the new process gets the current default error mode. An application sets the current default error mode by calling 
<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>. 




This flag is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW_CONSOLE"></a><a id="create_new_console"></a><dl>
<dt><b>CREATE_NEW_CONSOLE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The new process has a new console, instead of inheriting the parent's console. This flag cannot be used with the DETACHED_PROCESS flag. 




This flag is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW_PROCESS_GROUP"></a><a id="create_new_process_group"></a><dl>
<dt><b>CREATE_NEW_PROCESS_GROUP</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The new process is the root process of a new process group. The process group includes all processes that are descendants of this root process. The process identifier of the new process group is the same as the process identifier, which is returned in the <i>lpProcessInfo</i> parameter. Process groups are used by the 
<a href="base.generateconsolectrlevent">GenerateConsoleCtrlEvent</a> function to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes. 




This flag is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_SEPARATE_WOW_VDM"></a><a id="create_separate_wow_vdm"></a><dl>
<dt><b>CREATE_SEPARATE_WOW_VDM</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
This flag is only valid starting a 16-bit Windows-based application. If set, the new process runs in a private Virtual DOS Machine (VDM). By default, all 16-bit Windows-based applications run in a single, shared VDM. The advantage of running separately is that a crash only terminates the single VDM; any other programs running in distinct VDMs continue to function normally. Also, 16-bit Windows-based applications that run in separate VDMs have separate input queues. That means that if one application stops responding momentarily, applications in separate VDMs continue to receive input.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_SUSPENDED"></a><a id="create_suspended"></a><dl>
<dt><b>CREATE_SUSPENDED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The primary thread of the new process is created in a suspended state, and does not run until the 
<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a> function is called.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_UNICODE_ENVIRONMENT"></a><a id="create_unicode_environment"></a><dl>
<dt><b>CREATE_UNICODE_ENVIRONMENT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Indicates the format of the <i>lpEnvironment</i> parameter. If this flag is set, the environment block pointed to by <i>lpEnvironment</i> uses Unicode characters. Otherwise, the environment block uses ANSI characters.

</td>
</tr>
<tr>
<td width="40%"><a id="EXTENDED_STARTUPINFO_PRESENT"></a><a id="extended_startupinfo_present"></a><dl>
<dt><b>EXTENDED_STARTUPINFO_PRESENT</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The process is created with extended startup information; the <i>lpStartupInfo</i> parameter specifies a <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure.

<b>Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
</table>
 

This parameter also controls the new process's priority class, which is used to determine the scheduling priorities of the process's threads. For a list of values, see 
<a href="https://msdn.microsoft.com/2a16b18f-8efa-43f0-9f7d-d38cc8a153d3">GetPriorityClass</a>. If none of the priority class flags is specified, the priority class defaults to NORMAL_PRIORITY_CLASS unless the priority class of the creating process is IDLE_PRIORITY_CLASS or BELOW_NORMAL_PRIORITY_CLASS. In this case, the child process receives the default priority class of the calling process.


### -param lpEnvironment [in, optional]

A pointer to an environment block for the new process. If this parameter is NULL, the new process uses an environment created from the profile of the user specified by <i>lpUsername</i>. 




An environment block consists of a null-terminated block of null-terminated strings. Each string is in the following form:

<i>name</i>=<i>value</i>

Because the equal sign (=) is used as a separator, it must not be used in the name of an environment variable.

An environment block can contain Unicode or ANSI characters. If the environment block pointed to by <i>lpEnvironment</i> contains Unicode characters, be sure that <i>dwCreationFlags</i> includes CREATE_UNICODE_ENVIRONMENT.  If this parameter is NULL and the environment block of the parent process contains Unicode characters, you must also ensure that <i>dwCreationFlags</i> includes CREATE_UNICODE_ENVIRONMENT.

An ANSI environment block is terminated by two zero bytes: one for the last string, one more to terminate the block. A Unicode environment block is terminated by four zero bytes: two for the last string and two more to terminate the block.

To retrieve a copy of the environment block for a specific user, use the 
<a href="_shell_createenvironmentblock">CreateEnvironmentBlock</a> function.


### -param lpCurrentDirectory [in, optional]

The full path to the current directory for the process. The string can also specify a UNC path. 

If this parameter is NULL, the new process will have the same current drive and directory as the calling process. (This feature is provided primarily for shells that need to start an application and specify its initial drive and working directory.)


### -param lpStartupInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure. 




If the <b>lpDesktop</b> member is NULL or an empty string, the new process inherits the desktop and window station of its parent process. The function adds permission for the specified user account to the inherited window station and desktop. Otherwise, if this member specifies a desktop, it is the responsibility of the application to add permission for the specified user account to the specified window station and desktop, even for WinSta0\Default.

Handles in 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> or <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> must be closed with 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when they are no longer needed.

<div class="alert"><b>Important</b>  If the <b>dwFlags</b> member of the  <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure specifies <b>STARTF_USESTDHANDLES</b>, the standard handle fields are copied unchanged to the child process without validation. The caller is responsible for ensuring that these fields contain valid handle values.  Incorrect values can cause the child process to misbehave or crash. Use the <a href="http://go.microsoft.com/fwlink/p/?linkid=234779">Application Verifier</a> runtime verification tool to detect invalid handles. </div>
<div> </div>

### -param lpProcessInformation [out]

A pointer to a 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure that receives identification information for the new process, including a handle to the process. 




Handles in 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> must be closed with the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function when they are no longer needed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Note that the function returns before the process has finished initialization. If a required DLL cannot be located or fails to initialize, the process is terminated. To get the termination status of a process, call <a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>. 




## -remarks



By default, 
<b>CreateProcessWithTokenW</b> does not load the specified user's profile into the <b>HKEY_USERS</b> registry key. This means that access to information in the  <b>HKEY_CURRENT_USER</b> registry key may not produce results consistent with a normal interactive logon. It is your responsibility to load the user's registry hive into <b>HKEY_USERS</b>  by either using LOGON_WITH_PROFILE, or by calling the 
<a href="_shell_loaduserprofile">LoadUserProfile</a> function before calling this function.

If the <i>lpEnvironment</i> parameter is NULL, the new process uses an environment block created from the profile of the user specified by <i>lpUserName</i>. If the HOMEDRIVE and HOMEPATH variables are not set, <b>CreateProcessWithTokenW</b> modifies the environment block to use the drive and path of the user's working directory.

When created, the new process and thread handles receive full access rights (PROCESS_ALL_ACCESS and THREAD_ALL_ACCESS). For either handle, if a security descriptor is not provided, the handle can be used in any function that requires an object handle of that type. When a security descriptor is provided, an access check is performed on all subsequent uses of the handle before access is granted. If access is denied, the requesting process cannot use the handle to gain access to the process or thread.

To retrieve a security token, pass the process handle in the 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure to the 
<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a> function.

The process is assigned a process identifier. The identifier is valid until the process terminates. It can be used to identify the process, or specified in the 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function to open a handle to the process. The initial thread in the process is also assigned a thread identifier. It can be specified in the 
<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function to open a handle to the thread. The identifier is valid until the thread terminates and can be used to uniquely identify the thread within the system. These identifiers are returned in 
<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a>.

The calling thread can use the 
<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> function to wait until the new process has finished its initialization and is waiting for user input with no input pending. This can be useful for synchronization between parent and child processes, because 
<b>CreateProcessWithTokenW</b> returns without waiting for the new process to finish its initialization. For example, the creating process would use 
<b>WaitForInputIdle</b> before trying to find a window associated with the new process.

The preferred way to shut down a process is by using the 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> function, because this function sends notification of approaching termination to all DLLs attached to the process. Other means of shutting down a process do not notify the attached DLLs. Note that when a thread calls 
<b>ExitProcess</b>, other threads of the process are terminated without an opportunity to execute any additional code (including the thread termination code of attached DLLs). For more information, see 
<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The <i>lpApplicationName</i> parameter can be NULL, in which case the executable name must be the first white space–delimited string in <i>lpCommandLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. The following example is dangerous because the function will attempt to run "Program.exe", if it exists, instead of "MyApp.exe".

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline = L"C:\\Program Files\\MyApp";
	CreateProcessWithTokenW(/*...*/, szCmdline, /*...*/);</code></pre>
If a malicious user were to create an application called "Program.exe" on a system, any program that incorrectly calls 
<b>CreateProcessWithTokenW</b> using the Program Files directory will run this application instead of the intended application.

To avoid this problem, do not pass NULL for <i>lpApplicationName</i>. If you do pass NULL for <i>lpApplicationName</i>, use quotation marks around the executable path in <i>lpCommandLine</i>, as shown in the example below.

<pre class="syntax" xml:space="preserve"><code>	LPTSTR szCmdline = L"\"C:\\Program Files\\MyApp\"";
	CreateProcessWithTokenW(/*...*/, szCmdline, /*...*/);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="_shell_createenvironmentblock">CreateEnvironmentBlock</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/fb431d83-f3e7-4f2a-bad9-81259681c1f4">GetEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a>
 

 

