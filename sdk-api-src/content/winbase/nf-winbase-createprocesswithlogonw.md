---
UID: NF:winbase.CreateProcessWithLogonW
title: CreateProcessWithLogonW function (winbase.h)
description: Creates a new process and its primary thread. Then the new process runs the specified executable file in the security context of the specified credentials (user, domain, and password). It can optionally load the user profile for a specified user.
helpviewer_keywords: ["CREATE_DEFAULT_ERROR_MODE","CREATE_NEW_CONSOLE","CREATE_NEW_PROCESS_GROUP","CREATE_SEPARATE_WOW_VDM","CREATE_SUSPENDED","CREATE_UNICODE_ENVIRONMENT","CreateProcessWithLogonW","CreateProcessWithLogonW function","LOGON_NETCREDENTIALS_ONLY","LOGON_WITH_PROFILE","_win32_createprocesswithlogonw","base.createprocesswithlogonw","winbase/CreateProcessWithLogonW"]
old-location: base\createprocesswithlogonw.htm
tech.root: backup
ms.assetid: dcfdcd5b-0269-4081-b1db-e272171c27a2
ms.date: 12/05/2018
ms.keywords: CREATE_DEFAULT_ERROR_MODE, CREATE_NEW_CONSOLE, CREATE_NEW_PROCESS_GROUP, CREATE_SEPARATE_WOW_VDM, CREATE_SUSPENDED, CREATE_UNICODE_ENVIRONMENT, CreateProcessWithLogonW, CreateProcessWithLogonW function, LOGON_NETCREDENTIALS_ONLY, LOGON_WITH_PROFILE, _win32_createprocesswithlogonw, base.createprocesswithlogonw, winbase/CreateProcessWithLogonW
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateProcessWithLogonW
 - winbase/CreateProcessWithLogonW
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
 - CreateProcessWithLogonW
---

# CreateProcessWithLogonW function


## -description

Creates a new process and its primary thread. Then the new process runs the specified executable file in the security context of the specified credentials (user, domain, and password). It can optionally load the user profile for a specified user.

This function is similar to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> and <a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithtokenw">CreateProcessWithTokenW</a> functions, except that the caller does not need to call the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function to authenticate the user and get a token.

## -parameters

### -param lpUsername [in]

The name of the user. This is the name of the user account to log on to. If you use the UPN format, <i>user</i>@<i>DNS_domain_name</i>, the <i>lpDomain</i> parameter must be NULL. 




The user account must have the Log On Locally permission on the local computer. This permission is granted to all users on workstations and servers, but only to administrators on domain controllers.

### -param lpDomain [in, optional]

The name of the domain or server whose account database contains the <i>lpUsername</i> account. If this parameter is NULL, the user name must be specified in UPN format.

### -param lpPassword [in]

The clear-text password for the <i>lpUsername</i> account.

### -param dwLogonFlags [in]

The logon option. This parameter can be 0 (zero) or one of the following values.

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
Log on, then load the user profile in the <b>HKEY_USERS</b> registry key. The function returns after the profile is loaded. Loading the profile can be time-consuming, so it is best to use this value only if you must access the information in the <b>HKEY_CURRENT_USER</b> registry key. 




<b>Windows Server 2003:  </b>The profile is unloaded after the new process is terminated, whether or not it has created child processes.

<b>Windows XP:  </b>The profile is unloaded after the new process and all child processes it has created are terminated.

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




The string can specify the full path and file name of the module to execute or it can specify a partial name. If it is a partial name, the function uses the current drive and current directory to complete the specification. The function does not use the search path. This parameter must include the file name extension; no default extension is assumed.

The <i>lpApplicationName</i> parameter can be NULL, and the module name must be the first white space–delimited token in the <i>lpCommandLine</i> string. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin; otherwise, the file name is ambiguous.

For example, the following string can be interpreted in different ways:

"c:\program files\sub dir\program name"

The system tries to interpret the possibilities in the following order:<ol>
<li><b>c:\program.exe</b> files\sub dir\program name</li>
<li><b>c:\program files\sub.exe</b> dir\program name</li>
<li><b>c:\program files\sub dir\program.exe</b> name</li>
<li><b>c:\program files\sub dir\program name.exe</b></li>
</ol>


If the executable module is a 16-bit application, <i>lpApplicationName</i> should be NULL, and the string pointed to by <i>lpCommandLine</i> should specify the executable module and its arguments.

### -param lpCommandLine [in, out, optional]

The command line to be executed. The maximum length of this string is 1024 characters. If <i>lpApplicationName</i> is <b>NULL</b>, the module name portion of <i>lpCommandLine</i> is limited to <b>MAX_PATH</b> characters.

The function can modify the contents of this string. Therefore, this parameter cannot be a pointer to read-only memory (such as a <b>const</b> variable or a literal string). If this parameter is a constant string, the function may cause an access violation.

The <i>lpCommandLine</i> parameter can be <b>NULL</b>, and the function uses the string pointed to by <i>lpApplicationName</i> as the command line.

If both <i>lpApplicationName</i> and <i>lpCommandLine</i> are non-<b>NULL</b>, *<i>lpApplicationName</i> specifies the module to execute, and *<i>lpCommandLine</i> specifies the command line. The new process can use 
<a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a> to retrieve the entire command line. Console processes written in C can use the <i>argc</i> and <i>argv</i> arguments to parse the command line. Because <i>argv[0]</i> is the module name, C programmers typically repeat the module name as the first token in the command line.

If <i>lpApplicationName</i> is <b>NULL</b>, the first white space–delimited token of the command line specifies the module name. If you are using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin (see the explanation for the <i>lpApplicationName</i> parameter). If the file name does not contain an extension, .exe is appended. Therefore, if the file name extension is .com, this parameter must include the .com extension. If the file name ends in a period  with no extension, or if the file name contains a path, .exe is not appended. If the file name does not contain a directory path, the system searches for the executable file in the following sequence:

<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory for the parent process.</li>
<li>The 32-bit Windows system directory. Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a> function to get the path of this directory.</li>
<li>The 16-bit Windows system directory. There is no function that obtains the path of this directory, but it is searched.</li>
<li>The Windows directory. Use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable. Note that this function does not search the per-application path specified by the <b>App Paths</b> registry key. To include this per-application path in the search sequence, use the <a href="/windows/win32/api/shellapi/nf-shellapi-shellexecutew">ShellExecute</a> function.</li>
</ol>
The system adds a null character to the command line string to separate the file name from the arguments. This divides the original string into two strings for internal processing.

### -param dwCreationFlags [in]

The flags that control how the process is created. The <b>CREATE_DEFAULT_ERROR_MODE</b>, <b>CREATE_NEW_CONSOLE</b>, and <b>CREATE_NEW_PROCESS_GROUP</b> flags are enabled by default. For a list of values, see <a href="/windows/desktop/ProcThread/process-creation-flags">Process Creation Flags</a>.


This parameter also controls the new process's priority class, which is used to determine the scheduling priorities of the process's threads. For a list of values, see 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>. If none of the priority class flags is specified, the priority class defaults to <b>NORMAL_PRIORITY_CLASS</b> unless the priority class of the creating process is <b>IDLE_PRIORITY_CLASS</b> or <b>BELOW_NORMAL_PRIORITY_CLASS</b>. In this case, the child process receives the default priority class of the calling process.

If the dwCreationFlags parameter has a value of 0:

- The process gets the default error mode, creates a new console and creates a new process group. 
- The environment block for the new process is assumed to contain ANSI characters (see *lpEnvironment* parameter for additional information).
- A 16-bit Windows-based application runs in a shared Virtual DOS machine (VDM).

### -param lpEnvironment [in, optional]

A pointer to an environment block for the new process. If this parameter is <b>NULL</b>, the new process uses an environment created from the profile of the user specified by <i>lpUsername</i>. 




An environment block consists of a null-terminated block of null-terminated strings. Each string is in the following form:

<i>name</i>=<i>value</i>

Because the equal sign (=) is used as a separator, it must not be used in the name of an environment variable.

An environment block can contain Unicode or ANSI characters. If the environment block pointed to by <i>lpEnvironment</i> contains Unicode characters, ensure that <i>dwCreationFlags</i> includes <b>CREATE_UNICODE_ENVIRONMENT</b>.

An ANSI environment block is terminated by two 0 (zero) bytes: one for the last string and one more to terminate the block. A Unicode environment block is terminated by four zero bytes: two for the last string and two more to terminate the block.

To retrieve a copy of the environment block for a specific user, use the 
<a href="/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a> function.

### -param lpCurrentDirectory [in, optional]

The full path to the current directory for the process. The string can also specify a UNC path. 

If this parameter is <b>NULL</b>, the new process has the same current drive and directory as the calling process. This feature is provided primarily for shells that need to start an application, and specify its initial drive and working directory.

### -param lpStartupInfo [in]

A pointer to a 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure. 


The application must add permission for the specified user account to the specified window station and desktop, even for WinSta0\Default.

If the <b>lpDesktop</b> member is <b>NULL</b> or an empty string, the new process inherits the desktop and window station of its parent process. 
The application must add permission for the specified user account to the inherited window station and desktop.

<b>Windows XP:  </b><b>CreateProcessWithLogonW</b> adds permission for the specified user account to the inherited window station and desktop. 

Handles in 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> must be closed with 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> when they are no longer needed.

<div class="alert"><b>Important</b>  If the <b>dwFlags</b> member of the  <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure specifies <b>STARTF_USESTDHANDLES</b>, the standard handle fields are copied unchanged to the child process without validation. The caller is responsible for ensuring that these fields contain valid handle values.  Incorrect values can cause the child process to misbehave or crash. Use the <a href="/windows-hardware/drivers/devtest/application-verifier">Application Verifier</a> runtime verification tool to detect invalid handles. </div>
<div> </div>

### -param lpProcessInformation [out]

A pointer to a 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> structure that receives identification information for the new process, including a handle to the process. 




Handles in 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> must be closed with the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function when they are not needed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Note that the function returns before the process has finished initialization. If a required DLL cannot be located or fails to initialize, the process is terminated. To get the termination status of a process, call <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>.

## -remarks

By default, 
<b>CreateProcessWithLogonW</b> does not load the specified user profile into the <b>HKEY_USERS</b> registry key. This means that access to information in the <b>HKEY_CURRENT_USER</b> registry key may not produce results that are consistent with a normal interactive logon. It is your responsibility to load the user registry hive into <b>HKEY_USERS</b> before calling 
<b>CreateProcessWithLogonW</b>, by using <b>LOGON_WITH_PROFILE</b>, or by calling the 
<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> function.

If the <i>lpEnvironment</i> parameter is NULL, the new process uses an environment block created from the profile of the user specified by <i>lpUserName</i>. If the HOMEDRIVE and HOMEPATH variables are not set, <b>CreateProcessWithLogonW</b> modifies the environment block to use the drive and path of the user's working directory.

When created, the new process and thread handles receive full access rights (<b>PROCESS_ALL_ACCESS</b> and <b>THREAD_ALL_ACCESS</b>). For either handle, if a security descriptor is not provided, the handle can be used in any function that requires an object handle of that type. When a security descriptor is provided, an access check is performed on all subsequent uses of the handle before access is granted. If access is denied, the requesting process cannot use the handle to gain access to the process or thread.

To retrieve a security token, pass the process handle in the 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> structure to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a> function.

The process is assigned a process identifier. The identifier is valid until the process terminates. It can be used to identify the process, or it can be specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function to open a handle to the process. The initial thread in the process is also assigned a thread identifier. It can be specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function to open a handle to the thread. The identifier is valid until the thread terminates and can be used to uniquely identify the thread within the system. These identifiers are returned in 
<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a>.

The calling thread can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a> function to wait until the new process has completed its initialization and is waiting for user input with no input pending. This can be useful for synchronization between parent and child processes, because 
<b>CreateProcessWithLogonW</b> returns without waiting for the new process to finish its initialization. For example, the creating process would use 
<b>WaitForInputIdle</b> before trying to find a window that is associated with the new process.

The preferred way to shut down a process is by using the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a> function, because this function sends notification of approaching termination to all DLLs attached to the process. Other means of shutting down a process do not notify the attached DLLs. Note that when a thread calls 
<b>ExitProcess</b>, other threads of the process are terminated without an opportunity to execute any additional code (including the thread termination code of attached DLLs). For more information, see 
<a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>.

<b>CreateProcessWithLogonW</b> accesses the specified directory and executable image in the security context of the target user. If the executable image is on a network and a network drive letter is specified in the path, the network drive letter is not available to the target user, as network drive letters can be assigned for each logon. If a network drive letter is specified, this function fails. If the executable image is on a network, use the UNC path.

There is a limit to the number of child processes that can be created by this function and run simultaneously. For example, on Windows XP, this limit is <b>MAXIMUM_WAIT_OBJECTS</b>*4. However, you may not be able to create this many processes due to system-wide quota limits.

<b>Windows XP with SP2,Windows Server 2003, or later:  </b>You cannot call <b>CreateProcessWithLogonW</b> from a process that is running under the "LocalSystem" account,  because the function uses the logon SID in the caller token, and the token for the "LocalSystem" account does not contain this SID. As an alternative, use the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> and <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> functions.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The <i>lpApplicationName</i> parameter can be <b>NULL</b>, and  the executable name must be the first white space–delimited string in <i>lpCommandLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. Avoid the following example, because the function attempts to run "Program.exe", if it exists, instead of "MyApp.exe".


``` syntax
LPTSTR szCmdline[]=_tcsdup(TEXT("C:\\Program Files\\MyApp"));
CreateProcessWithLogonW(..., szCmdline, ...)
```

If a malicious user creates an application called "Program.exe" on a system, any program that incorrectly calls 
<b>CreateProcessWithLogonW</b> using the Program Files directory runs the malicious user application instead of the intended application.

To avoid this issue, do not pass <b>NULL</b> for <i>lpApplicationName</i>. If you pass <b>NULL</b> for <i>lpApplicationName</i>, use quotation marks around the executable path in <i>lpCommandLine</i>, as shown in the following example:


``` syntax
LPTSTR szCmdline[]=_tcsdup(TEXT("\"C:\\Program Files\\MyApp\""));
CreateProcessWithLogonW(..., szCmdline, ...)
```


#### Examples

The following example demonstrates how to call this function.


```cpp

#include <windows.h>
#include <stdio.h>
#include <userenv.h>

void DisplayError(LPWSTR pszAPI)
{
    LPVOID lpvMessageBuffer;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM,
        NULL, GetLastError(), 
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
        (LPWSTR)&lpvMessageBuffer, 0, NULL);

    //
    //... now display this string
    //
    wprintf(L"ERROR: API        = %s.\n", pszAPI);
    wprintf(L"       error code = %d.\n", GetLastError());
    wprintf(L"       message    = %s.\n", (LPWSTR)lpvMessageBuffer);

    //
    // Free the buffer allocated by the system
    //
    LocalFree(lpvMessageBuffer);

    ExitProcess(GetLastError());
}

void wmain(int argc, WCHAR *argv[])
{
    DWORD     dwSize;
    HANDLE    hToken;
    LPVOID    lpvEnv;
    PROCESS_INFORMATION pi = {0};
    STARTUPINFO         si = {0};
    WCHAR               szUserProfile[256] = L"";

    si.cb = sizeof(STARTUPINFO);
    
    if (argc != 4)
    {
        wprintf(L"Usage: %s [user@domain] [password] [cmd]", argv[0]);
        wprintf(L"\n\n");
        return;
    }

    //
    // TO DO: change NULL to '.' to use local account database
    //
    if (!LogonUser(argv[1], NULL, argv[2], LOGON32_LOGON_INTERACTIVE, 
            LOGON32_PROVIDER_DEFAULT, &hToken))
        DisplayError(L"LogonUser");

    if (!CreateEnvironmentBlock(&lpvEnv, hToken, TRUE))
        DisplayError(L"CreateEnvironmentBlock");

    dwSize = sizeof(szUserProfile)/sizeof(WCHAR);

    if (!GetUserProfileDirectory(hToken, szUserProfile, &dwSize))
        DisplayError(L"GetUserProfileDirectory");

    //
    // TO DO: change NULL to '.' to use local account database
    //
    if (!CreateProcessWithLogonW(argv[1], NULL, argv[2], 
            LOGON_WITH_PROFILE, NULL, argv[3], 
            CREATE_UNICODE_ENVIRONMENT, lpvEnv, szUserProfile, 
            &si, &pi))
        DisplayError(L"CreateProcessWithLogonW");

    if (!DestroyEnvironmentBlock(lpvEnv))
        DisplayError(L"DestroyEnvironmentBlock");

    CloseHandle(hToken);
    CloseHandle(pi.hProcess);
    CloseHandle(pi.hThread);
}

```

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



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
