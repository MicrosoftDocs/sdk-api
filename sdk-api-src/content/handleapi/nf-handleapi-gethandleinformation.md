---
UID: NF:handleapi.GetHandleInformation
title: GetHandleInformation function
author: windows-sdk-content
description: Retrieves certain properties of an object handle.
old-location: base\gethandleinformation.htm
tech.root: sysinfo
ms.assetid: a0f50a0d-739d-411b-8144-77b775476d26
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetHandleInformation, GetHandleInformation function, HANDLE_FLAG_INHERIT, HANDLE_FLAG_PROTECT_FROM_CLOSE, _win32_gethandleinformation, base.gethandleinformation, handleapi/GetHandleInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: handleapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - API-MS-Win-Core-handle-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetHandleInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetHandleInformation function


## -description


Retrieves certain properties of an object handle.


## -parameters




### -param hObject [in]

A handle to an object whose information is to be retrieved. 




You can specify a handle to one of the following types of objects: access token, console input buffer, console screen buffer, event, file, file mapping, job, mailslot, mutex, pipe, printer, process, registry key, semaphore, serial communication device, socket, thread, or waitable timer.


### -param lpdwFlags [out]

A pointer to a variable that receives a set of bit flags that specify properties of the object handle or 0. The following values are defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HANDLE_FLAG_INHERIT"></a><a id="handle_flag_inherit"></a><dl>
<dt><b>HANDLE_FLAG_INHERIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, a child process created with the <i>bInheritHandles</i> parameter of 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> set to <b>TRUE</b> will inherit the object handle.

</td>
</tr>
<tr>
<td width="40%"><a id="HANDLE_FLAG_PROTECT_FROM_CLOSE"></a><a id="handle_flag_protect_from_close"></a><dl>
<dt><b>HANDLE_FLAG_PROTECT_FROM_CLOSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function will not close the object handle.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/b4769e19-7478-4919-a9d2-8086ece6da70">Handle and
		  Object Functions</a>



<a href="https://msdn.microsoft.com/a3fa8b92-cba2-414e-9fb8-d0fcb98ede36">SetHandleInformation</a>
 

 

