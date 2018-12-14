---
UID: NS:processthreadsapi._PROCESS_INFORMATION
title: PROCESS_INFORMATION
author: windows-sdk-content
description: Contains information about a newly created process and its primary thread. It is used with the CreateProcess, CreateProcessAsUser, CreateProcessWithLogonW, or CreateProcessWithTokenW function.
old-location: base\process_information_str.htm
tech.root: procthread
ms.assetid: 78d84499-7e56-4ff7-a8cd-1cf1b275597a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPROCESS_INFORMATION, *PPROCESS_INFORMATION, LPPROCESS_INFORMATION, LPPROCESS_INFORMATION structure pointer, PROCESS_INFORMATION, PROCESS_INFORMATION structure, _win32_process_information_str, base.process_information_str, processthreadsapi/LPPROCESS_INFORMATION, processthreadsapi/PROCESS_INFORMATION, winbase/LPPROCESS_INFORMATION, winbase/PROCESS_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - processthreadsapi.h
api_name:
 - PROCESS_INFORMATION
product: Windows
targetos: Windows
req.typenames: PROCESS_INFORMATION, *PPROCESS_INFORMATION, *LPPROCESS_INFORMATION
req.redist: 
---

# PROCESS_INFORMATION structure


## -description


Contains information about a newly created process and its primary thread. It is used with the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>,  <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>, <a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>, or <a href="https://msdn.microsoft.com/b329866a-0c0d-4cb3-838c-36aac17c87ed">CreateProcessWithTokenW</a> function.


## -struct-fields




### -field hProcess

A handle to the newly created process. The handle is used to specify the process in all functions that perform operations on the process object.


### -field hThread

A handle to the primary thread of the newly created process. The handle is used to specify the thread in all functions that perform operations on the thread object.


### -field dwProcessId

A value that can be used to identify a process. The value is valid from the time the process is created until all handles to the process are closed and the process object is freed; at this point, the identifier may be reused.


### -field dwThreadId

A value that can be used to identify a thread. The value is valid from the time the thread is created until all handles to the thread are closed and the thread object is freed; at this point, the identifier may be reused.


## -remarks



If the function succeeds, be sure to call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the <b>hProcess</b> and <b>hThread</b> handles when you are finished with them. Otherwise, when the child process exits, the system cannot clean up the process structures for the child process because the parent process still has open handles to the child process. However, the system will close these handles when the parent process terminates, so the structures related to the child process object would be cleaned up at this point.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4">Creating Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/dcfdcd5b-0269-4081-b1db-e272171c27a2">CreateProcessWithLogonW</a>



<a href="https://msdn.microsoft.com/b329866a-0c0d-4cb3-838c-36aac17c87ed">CreateProcessWithTokenW</a>
 

 

