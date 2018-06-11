---
UID: NF:winbase.WinExec
title: WinExec function
author: windows-sdk-content
description: Runs the specified application.
old-location: base\winexec.htm
old-project: ProcThread
ms.assetid: 00ac3bd8-59d3-4f7f-8720-e57d05cee056
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: WinExec, WinExec function, _win32_winexec, base.winexec, winbase/WinExec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - WinExec
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinExec function


## -description


Runs the specified application.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows. Applications should use the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function.</div><div> </div>

## -parameters




### -param lpCmdLine [in]

The command line (file name plus optional parameters) for the application to be executed. If the name of the executable file in the <i>lpCmdLine</i> parameter does not contain a directory path, the system searches for the executable file in this sequence: 




<ol>
<li>The directory from which the application loaded.</li>
<li>The current directory.</li>
<li>The Windows system directory. The 
<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a> function retrieves the path of this directory.</li>
<li>The Windows directory. The 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function retrieves the path of this directory.</li>
<li>The directories listed in the PATH environment variable.</li>
</ol>

### -param uCmdShow [in]

The display options. For a list of the acceptable values, see the description of the <i>nCmdShow</i> parameter of the 
<a href="https://www.bing.com/search?q=ShowWindow">ShowWindow</a> function.


## -returns



If the function succeeds, the return value is greater than 31.

If the function fails, the return value is one of the following error values.

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
</dl>
</td>
<td width="60%">
The specified path was not found.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WinExec</b> function returns when the started process calls the <a href="https://www.bing.com/search?q=GetMessage">GetMessage</a> function or a time-out limit is reached. To avoid waiting for the time out delay, call the <b>GetMessage</b> function as soon as possible in any process started by a call to 
<b>WinExec</b>.

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
The executable name is treated as the first white space-delimited string in <i>lpCmdLine</i>. If the executable or path name has a space in it, there is a risk that a different executable could be run because of the way the function parses spaces. The following example is dangerous because the function will attempt to run "Program.exe", if it exists, instead of "MyApp.exe".

<pre class="syntax" xml:space="preserve"><code>WinExec("C:\\Program Files\\MyApp", ...)</code></pre>
If a malicious user were to create an application called "Program.exe" on a system, any program that incorrectly calls 
<b>WinExec</b> using the Program Files directory will run this application instead of the intended application.

To avoid this problem, use 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> rather than 
<b>WinExec</b>. However, if you must use 
<b>WinExec</b> for legacy reasons, make sure the application name is enclosed in quotation marks as shown in the example below.

<pre class="syntax" xml:space="preserve"><code>WinExec("\"C:\\Program Files\\MyApp.exe\" -L -S", ...)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>
 

 

