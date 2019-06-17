---
UID: NS:processthreadsapi._PROCESS_INFORMATION
title: PROCESS_INFORMATION (processthreadsapi.h)
author: windows-sdk-content
description: Contains information about a newly created process and its primary thread. It is used with the CreateProcess, CreateProcessAsUser, CreateProcessWithLogonW, or CreateProcessWithTokenW function.
old-location: base\process_information_str.htm
tech.root: ProcThread
ms.assetid: 78d84499-7e56-4ff7-a8cd-1cf1b275597a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPPROCESS_INFORMATION, *PPROCESS_INFORMATION, LPPROCESS_INFORMATION, LPPROCESS_INFORMATION structure pointer, PROCESS_INFORMATION, PROCESS_INFORMATION structure, _win32_process_information_str, base.process_information_str, processthreadsapi/LPPROCESS_INFORMATION, processthreadsapi/PROCESS_INFORMATION, winbase/LPPROCESS_INFORMATION, winbase/PROCESS_INFORMATION"
ms.topic: struct
f1_keywords: ["processthreadsapi/PROCESS_INFORMATION"]
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
ms.custom: 19H1
---

# PROCESS_INFORMATION structure


## -description


Contains information about a newly created process and its primary thread. It is used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>,  <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprocesswithtokenw">CreateProcessWithTokenW</a> function.


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



If the function succeeds, be sure to call the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the <b>hProcess</b> and <b>hThread</b> handles when you are finished with them. Otherwise, when the child process exits, the system cannot clean up the process structures for the child process because the parent process still has open handles to the child process. However, the system will close these handles when the parent process terminates, so the structures related to the child process object would be cleaned up at this point.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/creating-processes">Creating Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprocesswithtokenw">CreateProcessWithTokenW</a>
 

 

