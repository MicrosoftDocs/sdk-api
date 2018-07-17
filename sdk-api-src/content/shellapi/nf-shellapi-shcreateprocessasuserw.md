---
UID: NF:shellapi.SHCreateProcessAsUserW
title: SHCreateProcessAsUserW function
author: windows-sdk-content
description: Creates a new user-mode process and its primary thread to run a specified executable file.
old-location: shell\SHCreateProcessAsUserW.htm
old-project: shell
ms.assetid: 78548eaf-6907-41e3-9c22-848d0d159085
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHCreateProcessAsUserW, SHCreateProcessAsUserW function [Windows Shell], _win32_SHCreateProcessAsUserW, _win32_SHCreateProcessAsUserW_cpp, shell.SHCreateProcessAsUserW, shellapi/SHCreateProcessAsUserW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHCreateProcessAsUserW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateProcessAsUserW
 - SHCreateProcessAsUserW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHCreateProcessAsUserW function


## -description


<p class="CCE_Message">[<b>SHCreateProcessAsUserW</b> is not implemented under Windows XP or later systems.]

Creates a new user-mode process and its primary thread to run a specified executable file.
		
            


## -parameters




### -param pscpi [in, out]

Type: <b>PSHCREATEPROCESSINFOW</b>

A pointer to an <a href="https://msdn.microsoft.com/f51d22c5-ea3e-4040-9761-7555f8f7e0aa">SHCREATEPROCESSINFOW</a> structure with information on how to create the process.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> if not. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is similar to <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> with <b>runas</b> as the verb. However, <b>SHCreateProcessAsUserW</b> creates a process that runs in the security context of the user represented by the <b>hUserToken</b> member of the structure pointed to by <i>pscpi</i>. The <b>lpProcessInformation</b> member can be used to return a <a href="https://msdn.microsoft.com/78d84499-7e56-4ff7-a8cd-1cf1b275597a">PROCESS_INFORMATION</a> structure with information on the new process.

The <b>runas</b> verb must be supported by the executable file's <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">file type</a>. The .exe file type supports <b>runas</b>. Use the <a href="https://msdn.microsoft.com/026b841d-b831-475e-a788-2c79801e20b8">AssocQueryString</a> function to check whether <b>runas</b> is supported by other file types. The following code fragment illustrates the syntax.
			
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>AssocQueryString(0, ASSOCSTR_COMMAND, pszFile, TEXT("runas"), NULL, &amp;cchVerb)</pre>
</td>
</tr>
</table></span></div>
For a discussion of how to use the Shell to launch applications, see <a href="https://msdn.microsoft.com/d774c3b2-4caf-460a-ac32-0ed603491d5f">Launching Applications</a>.

<b>SHCreateProcessAsUserW</b> is not supported under Windows XP. Users requiring similar functionality should examine <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>, <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>, <a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a> and <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>, carefully evaluating each based on required functionality and security. <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> can be used to extract information used with <b>CreateProcess</b>, if necessary.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>



<a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>
 

 

