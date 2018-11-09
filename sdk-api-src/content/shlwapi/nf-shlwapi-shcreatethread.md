---
UID: NF:shlwapi.SHCreateThread
title: SHCreateThread function
author: windows-sdk-content
description: Creates a thread.
old-location: shell\SHCreateThread.htm
tech.root: shell
ms.assetid: 2140e396-29cd-4665-b684-337170570b73
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SHCreateThread, SHCreateThread function [Windows Shell], _win32_SHCreateThread, shell.SHCreateThread, shlwapi/SHCreateThread
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - ShCore.dll
 - API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
 - SHCreateThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateThread function


## -description


Creates a thread.


## -parameters




### -param pfnThreadProc [in]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an application-defined function of the <a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">LPTHREAD_START_ROUTINE</a> type. If a new thread was successfully created, this application-defined function is called in the context of that thread. <b>SHCreateThread</b> does not wait for the function pointed to by this parameter to complete before returning to its caller.  The application-defined function's return value is the exit code of the thread.


### -param pData [in, optional]

Type: <b>void*</b>

A pointer to an optional application-defined data structure that contains initialization data. It is passed to the function pointed to by <i>pfnThreadProc</i> and, optionally, <i>pfnCallback</i>. This value can be <b>NULL</b>.


### -param flags [in]

Type: <b>SHCT_FLAGS</b>

The flags that control the behavior of the function. One or more of the <a href="https://msdn.microsoft.com/66cda866-7a39-4c5a-a795-a4c5c64cbab7">CTF</a> constants.


### -param pfnCallback [in, optional]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an optional application-defined function of the 
				 <a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">LPTHREAD_START_ROUTINE</a> type. This function is called 
				 in the context of the created thread before the function pointed to by 
				 <i>pfnThreadProc</i> is called. It will also receive <i>pData</i> as 
				 its argument. <b>SHCreateThread</b> will wait for the 
				 function pointed to by <i>pfnCallback</i> to return before returning to its caller. The 
				 return value of the function pointed to by <i>pfnCallback</i> is ignored.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the thread is successfully created, or <b>FALSE</b> otherwise. On failure, use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the specific error value as shown here.

                    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>if (!SHCreateThread(...))
{
    hr = HRESULT_FROM_WIN32( GetLastError() );
}
else
{
    ....
}</pre>
</td>
</tr>
</table></span></div>



## -remarks



The function pointed to by <i>pfnThreadProc</i> and <i>pfnCallback</i> must take the following form.

				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD WINAPI ThreadProc(LPVOID pData)
{
  ...
}</pre>
</td>
</tr>
</table></span></div>
The function name is arbitrary. The <i>pData</i> parameter points to an application-defined data structure with initialization information.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/6abca2df-832c-410b-93c7-5131e481e595">SHCreateThreadRef</a>



<a href="https://msdn.microsoft.com/307b284b-f493-4d24-a7be-17c150d62b34">SHGetThreadRef</a>



<a href="https://msdn.microsoft.com/7f3fd09b-baad-4019-a060-c68727aee61f">SHReleaseThreadRef</a>



<a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>



<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell and Common Controls Versions</a>
 

 

