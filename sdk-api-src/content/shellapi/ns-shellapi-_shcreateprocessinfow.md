---
UID: NS:shellapi._SHCREATEPROCESSINFOW
title: "_SHCREATEPROCESSINFOW"
author: windows-sdk-content
description: Contains the information needed by SHCreateProcessAsUserW to create a process.
old-location: shell\SHCREATEPROCESSINFOW_str.htm
old-project: shell
ms.assetid: f51d22c5-ea3e-4040-9761-7555f8f7e0aa
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PSHCREATEPROCESSINFOW, PSHCREATEPROCESSINFOW, PSHCREATEPROCESSINFOW structure pointer [Windows Shell], SEE_MASK_CLASSKEY, SEE_MASK_CLASSNAME, SEE_MASK_CONNECTNETDRV, SEE_MASK_DOENVSUBST, SEE_MASK_FLAG_DDEWAIT, SEE_MASK_FLAG_NO_UI, SEE_MASK_HMONITOR, SEE_MASK_NOCLOSEPROCESS, SEE_MASK_NO_CONSOLE, SEE_MASK_UNICODE, SHCREATEPROCESSINFOW, SHCREATEPROCESSINFOW structure [Windows Shell], _SHCREATEPROCESSINFOW, _win32_SHCREATEPROCESSINFOW_str, shell.SHCREATEPROCESSINFOW_str, shellapi/PSHCREATEPROCESSINFOW, shellapi/SHCREATEPROCESSINFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: SHCREATEPROCESSINFOW, *PSHCREATEPROCESSINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shellapi.h
api_name:
-	SHCREATEPROCESSINFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _SHCREATEPROCESSINFOW structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/78548eaf-6907-41e3-9c22-848d0d159085">SHCreateProcessAsUserW</a> is no longer implemented in Windows XP or later versions.]

Contains the information needed by <a href="https://msdn.microsoft.com/78548eaf-6907-41e3-9c22-848d0d159085">SHCreateProcessAsUserW</a> to create a process.
        
            


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of this structure.


### -field fMask

Type: <b>ULONG</b>

An array of flags that indicates the content and validity of the other structure members. This can be a combination of the following values.



#### SEE_MASK_CLASSKEY

Use the file's class registry key.



#### SEE_MASK_CLASSNAME

Use the file's class name.



#### SEE_MASK_CONNECTNETDRV

Validate the share and connect to a drive letter. The <b>pszFile</b> member is a UNC path of a file on a network.



#### SEE_MASK_DOENVSUBST

Expand any environment variables.



#### SEE_MASK_FLAG_DDEWAIT

Wait for the DDE conversation to terminate before returning.



#### SEE_MASK_FLAG_NO_UI

Do not display an error message box if an error occurs.



#### SEE_MASK_HMONITOR

Use this flag when specifying a monitor on multimonitor systems.



#### SEE_MASK_NOCLOSEPROCESS

The application will close the process. If the <b>lpProcessInformation</b> member is a valid <a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> pointer, and <b>SEE_MASK_NOCLOSEPROCESS</b> is set, the process will remain open when <a href="https://msdn.microsoft.com/78548eaf-6907-41e3-9c22-848d0d159085">SHCreateProcessAsUserW</a> returns. The <b>hProcess</b> and <b>hThread</b> members of the <b>PROCESS_INFORMATION</b> structure hold the process and thread handles, respectively. This flag is typically set to allow an application to find out when a process created with <b>SHCreateProcessAsUserW</b> terminates. In some cases, such as when execution is satisfied through a DDE conversation, no handle will be returned. The calling application is responsible for closing the handle when it is no longer needed. If this flag is not set, the process will be closed before <b>SHCreateProcessAsUserW</b> returns, even if <b>lpProcessInformation</b> is a valid pointer.



#### SEE_MASK_NO_CONSOLE

Create a console for the new process instead of having it inherit the parent's console. It is equivalent to using a CREATE_NEW_CONSOLE flag with <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.



#### SEE_MASK_UNICODE

Indicates a Unicode application.


### -field hwnd

Type: <b>HWND</b>

A parent window handle.


### -field pszFile

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the executable file on which <a href="https://msdn.microsoft.com/78548eaf-6907-41e3-9c22-848d0d159085">SHCreateProcessAsUserW</a> will perform the action specified by the <b>runas</b> verb. The <b>runas</b> verb must be supported by the file's class.

<div class="alert"><b>Note</b>   If the path is not included with the file name, the current directory is assumed.</div>
<div> </div>

### -field pszParameters

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string containing the application parameters. The parameters must be separated by spaces.


### -field pszCurrentDirectory

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that contains the current directory.


### -field hUserToken

Type: <b>HANDLE</b>

An <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">Access token</a> that can be used to represent a particular user. It is needed when there are multiple users for those folders that are treated as belonging to a single user. The calling application must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. For further discussion of access control issues, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.


### -field lpProcessAttributes

Type: <b>LPSECURITY_ATTRIBUTES</b>

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure with the security descriptor for the new process. It also specifies whether a child process can be inherited. If this parameter is set to <b>NULL</b>, the process will have a default security descriptor and the handle cannot be inherited.

<b>Security Warning:  </b>Using a security descriptor incorrectly can compromise the security of your application. For more information, see <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>.


### -field lpThreadAttributes

Type: <b>LPSECURITY_ATTRIBUTES</b>

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure with the security descriptor for the new thread. It also specifies whether a child process can be inherited. If this parameter is set to <b>NULL</b>, the process will have a default security descriptor and the handle cannot be inherited.

<b>Security Warning:  </b>Using a security descriptor incorrectly can compromise the security of your application. For more information, see <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>.


### -field bInheritHandles

Type: <b>BOOL</b>

An indicator for whether the new process inherits handles from the calling process. If set to <b>TRUE</b>, each inheritable open handle in the calling process is inherited by the new process. Inherited handles have the same value and access privileges as the original handles.


### -field dwCreationFlags

Type: <b>DWORD</b>

Flags that control the creation of the process and the priority class. For a list of the available flags, see <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>.


### -field lpStartupInfo

Type: <b>LPSTARTUPINFOW</b>

A pointer to a <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure that specifies how the main window for the new process should appear.


### -field lpProcessInformation

Type: <b>LPPROCESS_INFORMATION</b>

A pointer to a <a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure that receives information about the new process. Set this member to a valid structure pointer, and set the SEE_MASK_NOCLOSEPROCESS flag in the <b>fMask</b> member, and the process will remain open when the function returns. The <b>PROCESS_INFORMATION</b> structure's <b>hProcess</b> and <b>hThread</b> members will then hold the process and thread handles, respectively. Set this member to <b>NULL</b>, and the process will be closed before the function returns.


## -remarks



 To include double quotation marks in <b>pszParameters</b>, you must enclose each mark in a pair of quotation marks, as in the following example:

				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>sei.lpParameters = "An example: \"\"\"quoted text\"\"\"";</pre>
</td>
</tr>
</table></span></div>

				
                In this case, the application receives three parameters: <i>An, example:, and "quoted text"</i>.




## -see-also




<a href="https://msdn.microsoft.com/50e0dac3-b5dc-4d9f-8fd7-3a53a428166b">SHELLEXECUTEINFO</a>
 

 

