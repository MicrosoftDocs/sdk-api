---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBackgroundCopyJob2::SetNotifyCmdLine


## -description


Specifies a program to execute if the job enters the <b>BG_JOB_STATE_ERROR</b> or <b>BG_JOB_STATE_TRANSFERRED</b> state. BITS executes the program in the context of the user who called this method.


## -parameters




### -param Program




### -param Parameters






#### - pParameters [in]

Null-terminated string that contains the parameters of the program in <i>pProgram</i>. The first parameter must be the program in <i>pProgram</i> (use quotes if the path uses long file names). The <i>pParameters</i> parameter is limited to 4,000 characters, not including the null terminator. This parameter can be <b>NULL</b>.


#### - pProgram [in]

Null-terminated string that contains the program to execute. The <i>pProgram</i> parameter is limited to MAX_PATH characters, not including the null terminator. You should specify a full path to the program; the method will not use the search path to locate the program. 




To remove command line notification, set <i>pProgram</i> and <i>pParameters</i> to <b>NULL</b>. The method fails if <i>pProgram</i> is <b>NULL</b> and <i>pParameters</i> is non-<b>NULL</b>.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be <b>BG_JOB_STATE_CANCELLED</b> or <b>BG_JOB_STATE_ACKNOWLEDGED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProgram</i> or <i>pParameters</i> string is too long.

</td>
</tr>
</table>
 




## -remarks



BITS calls the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function to launch the program.

Your program should return an exit code of zero. If your program does not return an exit code of zero, BITS checks the state of the job. If the program did not cancel or complete the job, BITS calls the program again after the <a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">minimum retry delay</a> specified for the job expires.

<b>BITS 1.5 and earlier:  </b>BITS calls the program only once. 

To execute a script, specify WScript.exe (include the full path to WScript.exe) in <i>pProgram</i>. The <i>pParameters</i> parameter should include WScript.exe, the script name, and any arguments.

If your program requires job related information, you must pass this information as arguments. Do not include environment variables, such as %system32%, in <i>pProgram</i> or <i>pParameters</i> — they are not expanded.

You should include the full path to the program. If any of the arguments in <i>pParameters</i> include a path that uses long file names, such as the module name, use quotes around the path.

If the program you want to execute uses the reply or download file, the program must call the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method to make the files available to the client.

Call the 
<a href="https://msdn.microsoft.com/24aa6445-d7bd-4825-9121-402e63ae6f69">IBackgroundCopyJob::SetNotifyFlags</a> method to specify when to execute the program. You can request command line execution only for job error or transferred events, not job modification events. Note that BITS still executes the command line even if you call the 
<b>SetNotifyCmdLine</b> method after the event occurs.

If the BITS job is in a service account context (ie, networkservice/localsystem/localservice), no form of command-line callback will execute. 

If you call both the <b>SetNotifyCmdLine</b> method 
and the <a href="https://msdn.microsoft.com/34d51546-ec27-471f-9da5-3bec7ed4e1ea">IBackgroundCopyJob::SetNotifyInterface</a> method, BITS will execute the command line only if the notification interface becomes invalid or the notification method that BITS calls returns a failure  code. For example, if the notification method that BITS calls returns a E_FAIL, BITS will execute the command line. However, if the notification method returns <b>S_OK</b>, BITS will not execute the command line. If the  notification method and command line execution request both fail, BITS will send the notification again after the minimum retry period expires. 

Note that calling the 
<a href="https://msdn.microsoft.com/12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0">IBackgroundCopyJob::TakeOwnership</a> method removes command line notification from the job.


#### Examples

For an example that calls the 
<b>SetNotifyCmdLine</b> method, see 
<a href="https://msdn.microsoft.com/f1996d08-0e35-403b-9cdb-dae9e1c42e05">Registering to Execute a Program</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/62978315-e893-4617-8e6d-63bab8204913">IBackgroundCopyJob2::GetNotifyCmdLine</a>



<a href="https://msdn.microsoft.com/24aa6445-d7bd-4825-9121-402e63ae6f69">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="https://msdn.microsoft.com/34d51546-ec27-471f-9da5-3bec7ed4e1ea">IBackgroundCopyJob::SetNotifyInterface</a>
 

 

