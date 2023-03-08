---
UID: NF:winbase.CreateProcessWithTokenW
title: CreateProcessWithTokenW function (winbase.h)
description: Creates a new process and its primary thread. The new process runs in the security context of the specified token. It can optionally load the user profile for the specified user.
helpviewer_keywords: ["CREATE_DEFAULT_ERROR_MODE","CREATE_NEW_CONSOLE","CREATE_NEW_PROCESS_GROUP","CREATE_SEPARATE_WOW_VDM","CREATE_SUSPENDED","CREATE_UNICODE_ENVIRONMENT","CreateProcessWithTokenW","CreateProcessWithTokenW function","EXTENDED_STARTUPINFO_PRESENT","LOGON_NETCREDENTIALS_ONLY","LOGON_WITH_PROFILE","base.createprocesswithtokenw","winbase/CreateProcessWithTokenW"]
old-location: base\createprocesswithtokenw.htm
tech.root: backup
ms.assetid: b329866a-0c0d-4cb3-838c-36aac17c87ed
ms.date: 12/05/2018
ms.keywords: CREATE_DEFAULT_ERROR_MODE, CREATE_NEW_CONSOLE, CREATE_NEW_PROCESS_GROUP, CREATE_SEPARATE_WOW_VDM, CREATE_SUSPENDED, CREATE_UNICODE_ENVIRONMENT, CreateProcessWithTokenW, CreateProcessWithTokenW function, EXTENDED_STARTUPINFO_PRESENT, LOGON_NETCREDENTIALS_ONLY, LOGON_WITH_PROFILE, base.createprocesswithtokenw, winbase/CreateProcessWithTokenW
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateProcessWithTokenW
 - winbase/CreateProcessWithTokenW
dev_langs:
 - c++
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
---

# CreateProcessWithTokenW function


## -description

Creates a new process and its primary thread. The new process runs in the security context of the specified token. It can optionally load the user profile for the specified user.

The process that calls <b>CreateProcessWithTokenW</b> must have the SE_IMPERSONATE_NAME privilege. If this function fails with ERROR_PRIVILEGE_NOT_HELD (1314), use the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> or <a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a> function instead. Typically, the process that calls  
<b>CreateProcessAsUser</b>  must have the SE_INCREASE_QUOTA_NAME privilege and may require the SE_ASSIGNPRIMARYTOKEN_NAME privilege if the token is  not assignable.    <b>CreateProcessWithLogonW</b> requires no special privileges, but the specified user account must be allowed to log on interactively. Generally, it is best to use <b>CreateProcessWithLogonW</b> to create a process with alternate credentials.

## -parameters

### -param hToken [in]

A handle to the primary token that represents a user. The handle must have the TOKEN_QUERY, TOKEN_DUPLICATE, and TOKEN_ASSIGN_PRIMARY access rights. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>. The user represented by the token must have read and execute access to the application specified by the <i>lpApplicationName</i> or the <i>lpCommandLine</i> parameter. 




To get a primary token that represents the specified user, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function. Alternatively, you can call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a> function to convert an impersonation token into a primary token. This allows a server application that is impersonating a client to create a process that has the security context of the client.

<b>Terminal Services:  </b>The caller's process always runs in the caller's session, not in the session specified in the token. To run a process in the session specified in the token, use the CreateProcessAsUser function.

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
<a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a> to retrieve the entire command line. Console processes written in C can use the <i>argc</i> and <i>argv</i> arguments to parse the command line. Because argv[0] is the module name, C programmers generally repeat the module name as the first token in the command line.

If <i>lpApplicationName</i> is NULL, the first white space–delimited token of the command line specifies the module name. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin (see the explanation for the <i>lpApplicationName</i> parameter). If the file name does not contain an extension, .exe is appended. Therefore, if the file name extension is .com, this parameter must include the .com extension. If the file name ends in a period (.) with no extension, or if the file name contains a path, .exe is not appended. If the file name does not contain a directory path, the system searches for the executable file in the following sequence:

<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory for the parent process.</li>
<li>The 32-bit Windows system directory. Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a> function to get the path of this directory.</li>
<li>The 16-bit Windows system directory. There is no function that obtains the path of this directory, but it is searched.</li>
<li>The Windows directory. Use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable. Note that this function does not search the per-application path specified by the <b>App Paths</b> registry key. To include this per-application path in the search sequence, use the <a href="/previous-versions/windows/desktop/axe/shellexecute">ShellExecute</a> function.</li>
</ol>
The system adds a null character to the command line string to separate the file name from the arguments. This divides the original string into two strings for internal processing.

### -param dwCreationFlags [in]

The flags that control how the process is created. The CREATE_DEFAULT_ERROR_MODE, CREATE_NEW_CONSOLE, and CREATE_NEW_PROCESS_GROUP flags are enabled by default. For a list of values, see <a href="/windows/desktop/ProcThread/process-creation-flags">Process Creation Flags</a>.


This parameter also controls the new process's priority class, which is used to determine the scheduling priorities of the process's threads. For a list of values, see 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>. If none of the priority class flags is specified, the priority class defaults to NORMAL_PRIORITY_CLASS unless the priority class of the creating process is IDLE_PRIORITY_CLASS or BELOW_NORMAL_PRIORITY_CLASS. In this case, the child process receives the default priority class of the calling process.

If the dwCreationFlags parameter has a value of 0:

- The process gets the default error mode, creates a new console and creates a new process group. 
- The environment block for the new process is assumed to contain ANSI characters (see *lpEnvironment* parameter for additional information).
- A 16-bit Windows-based application runs in a shared Virtual DOS machine (VDM).

### -param lpEnvironment [in, optional]

A pointer to an environment block for the new process. If this parameter is NULL, the new process uses an environment created from the profile of the user specified by <i>lpUsername</i>. 




An environment block consists of a null-terminated block of null-terminated strings. Each string is in the following form:

<i>name</i>=<i>value</i>

Because the equal sign (=) is used as a separator, it must not be used in the name of an environment variable.

An environment block can contain Unicode or ANSI characters. If the environment block pointed to by <i>lpEnvironment</i> contains Unicode characters, be sure that <i>dwCreationFlags</i> includes CREATE_UNICODE_ENVIRONMENT.

An ANSI environment block is terminated by two zero bytes: one for the last string, one more to terminate the block. A Unicode environment block is terminated by four zero bytes: two for the last string and two more to terminate the block.

To retrieve a copy of the environment block for a specific user, use the 
<a href="/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a> function.

### -param lpCurrentDirectory [in, optional]

The full path to the current directory for the process. The string can also specify a UNC path. 

If this parameter is NULL, the new process will have the same current drive and directory as the calling process. (This feature is provided primarily for shells that need to start an application and specify its initial drive and working directory.)

### -param lpStartupInfo [in]

A pointer to a 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> or <a href="/windows/desktop/api/winbase/ns-winbase-startupinfoexa">STARTUPINFOEX</a> structure. 




If the <b>lpDesktop</b> member is NULL or an empty string, the new process inherits the desktop and window station of its parent process. The function adds permission for the specified user account to the inherited window station and desktop. Otherwise, if this member specifies a desktop, it is the responsibility of the application to add permission for the specified user account to the specified window station and desktop, even for WinSta0\Default.

Handles in 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> or <a href="/windows/desktop/api/winbase/ns-winbase-startupinfoexa">STARTUPINFOEX</a> must be closed with 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> when they are no longer needed.

<div class="alert"><b>Important</b>  If the <b>dwFlags</b> member of the  <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure specifies <b>STARTF_USESTDHANDLES</b>, the standard handle fields are copied unchanged to the child process without validation. The caller is responsible for ensuring that these fields contain valid handle values.  Incorrect values can cause the child process to misbehave or crash. Use the <a href="/windows-hardware/drivers/devtest/application-verifier">Application Verifier</a> runtime verification tool to detect invalid handles. </div>
<div> </div>

### -param lpProcessInformation [out]

A pointer to a 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> structure that receives identification information for the new process, including a handle to the process. 




Handles in 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> must be closed with the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function when they are no longer needed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Note that the function returns before the process has finished initialization. If a required DLL cannot be located or fails to initialize, the process is terminated. To get the termination status of a process, call <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>.

## -remarks

By default, 
<b>CreateProcessWithTokenW</b> does not load the specified user's profile into the <b>HKEY_USERS</b> registry key. This means that access to information in the  <b>HKEY_CURRENT_USER</b> registry key may not produce results consistent with a normal interactive logon. It is your responsibility to load the user's registry hive into <b>HKEY_USERS</b>  by either using LOGON_WITH_PROFILE, or by calling the 
<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> function before calling this function.

If the <i>lpEnvironment</i> parameter is NULL, the new process uses an environment block created from the profile of the user specified by <i>lpUserName</i>. If the HOMEDRIVE and HOMEPATH variables are not set, <b>CreateProcessWithTokenW</b> modifies the environment block to use the drive and path of the user's working directory.

When created, the new process and thread handles receive full access rights (PROCESS_ALL_ACCESS and THREAD_ALL_ACCESS). For either handle, if a security descriptor is not provided, the handle can be used in any function that requires an object handle of that type. When a security descriptor is provided, an access check is performed on all subsequent uses of the handle before access is granted. If access is denied, the requesting process cannot use the handle to gain access to the process or thread.

To retrieve a security token, pass the process handle in the 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> structure to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a> function.

The process is assigned a process identifier. The identifier is valid until the process terminates. It can be used to identify the process, or specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function to open a handle to the process. The initial thread in the process is also assigned a thread identifier. It can be specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function to open a handle to the thread. The identifier is valid until the thread terminates and can be used to uniquely identify the thread within the system. These identifiers are returned in 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a>.

The calling thread can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a> function to wait until the new process has finished its initialization and is waiting for user input with no input pending. This can be useful for synchronization between parent and child processes, because 
<b>CreateProcessWithTokenW</b> returns without waiting for the new process to finish its initialization. For example, the creating process would use 
<b>WaitForInputIdle</b> before trying to find a window associated with the new process.

The preferred way to shut down a process is by using the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a> function, because this function sends notification of approaching termination to all DLLs attached to the process. Other means of shutting down a process do not notify the attached DLLs. Note that when a thread calls 
<b>ExitProcess</b>, other threads of the process are terminated without an opportunity to execute any additional code (including the thread termination code of attached DLLs). For more information, see 
<a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The <i>lpApplicationName</i> parameter can be NULL, in which case the executable name must be the first white space–delimited string in <i>lpCommandLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. The following example is dangerous because the function will attempt to run "Program.exe", if it exists, instead of "MyApp.exe".


``` syntax
	LPTSTR szCmdline = L"C:\\Program Files\\MyApp";
	CreateProcessWithTokenW(/*...*/, szCmdline, /*...*/);
```

If a malicious user were to create an application called "Program.exe" on a system, any program that incorrectly calls 
<b>CreateProcessWithTokenW</b> using the Program Files directory will run this application instead of the intended application.

To avoid this problem, do not pass NULL for <i>lpApplicationName</i>. If you do pass NULL for <i>lpApplicationName</i>, use quotation marks around the executable path in <i>lpCommandLine</i>, as shown in the example below.


``` syntax
	LPTSTR szCmdline = L"\"C:\\Program Files\\MyApp\"";
	CreateProcessWithTokenW(/*...*/, szCmdline, /*...*/);
```


## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>



<a href="/windows/desktop/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">GetEnvironmentStrings</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a>



<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>



<a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a>
