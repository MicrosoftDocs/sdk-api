---
UID: NF:bits1_5.IBackgroundCopyJob2.SetNotifyCmdLine
title: IBackgroundCopyJob2::SetNotifyCmdLine
description: Specifies a program to execute if the job enters the BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSFERRED state. BITS executes the program in the context of the user who called this method.
helpviewer_keywords: ["IBackgroundCopyJob2 interface [BITS]","SetNotifyCmdLine method","IBackgroundCopyJob2.SetNotifyCmdLine","IBackgroundCopyJob2::SetNotifyCmdLine","SetNotifyCmdLine","SetNotifyCmdLine method [BITS]","SetNotifyCmdLine method [BITS]","IBackgroundCopyJob2 interface","_drz_ibackgroundcopyjob2_setnotifycmdline","bits.ibackgroundcopyjob2_setnotifycmdline","bits1_5/IBackgroundCopyJob2::SetNotifyCmdLine"]
old-location: bits\ibackgroundcopyjob2_setnotifycmdline.htm
tech.root: Bits
ms.assetid: 61b99d01-ca0f-4a89-b7ca-77d23c21a9ad
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2 interface [BITS],SetNotifyCmdLine method, IBackgroundCopyJob2.SetNotifyCmdLine, IBackgroundCopyJob2::SetNotifyCmdLine, SetNotifyCmdLine, SetNotifyCmdLine method [BITS], SetNotifyCmdLine method [BITS],IBackgroundCopyJob2 interface, _drz_ibackgroundcopyjob2_setnotifycmdline, bits.ibackgroundcopyjob2_setnotifycmdline, bits1_5/IBackgroundCopyJob2::SetNotifyCmdLine
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2::SetNotifyCmdLine
 - bits1_5/IBackgroundCopyJob2::SetNotifyCmdLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.SetNotifyCmdLine
---

# IBackgroundCopyJob2::SetNotifyCmdLine


## -description

Specifies a program to execute if the job enters the <b>BG_JOB_STATE_ERROR</b> or <b>BG_JOB_STATE_TRANSFERRED</b> state. BITS executes the program in the context of the user who called this method.

## -parameters

### -param Program [in]

Null-terminated string that contains the program to execute. The <i>pProgram</i> parameter is limited to MAX_PATH characters, not including the null terminator. You should specify a full path to the program; the method will not use the search path to locate the program. 




To remove command line notification, set <i>pProgram</i> and <i>pParameters</i> to <b>NULL</b>. The method fails if <i>pProgram</i> is <b>NULL</b> and <i>pParameters</i> is non-<b>NULL</b>.

### -param Parameters [in]

Null-terminated string that contains the parameters of the program in <i>pProgram</i>. The first parameter must be the program in <i>pProgram</i> (use quotes if the path uses long file names). The <i>pParameters</i> parameter is limited to 4,000 characters, not including the null terminator. This parameter can be <b>NULL</b>.

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
<dt><b>S_OK</b></dt>
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
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function to launch the program.

Your program should return an exit code of zero. If your program does not return an exit code of zero, BITS checks the state of the job. If the program did not cancel or complete the job, BITS calls the program again after the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay">minimum retry delay</a> specified for the job expires.

<b>BITS 1.5 and earlier:  </b>BITS calls the program only once. 

To execute a script, specify WScript.exe (include the full path to WScript.exe) in <i>pProgram</i>. The <i>pParameters</i> parameter should include WScript.exe, the script name, and any arguments.

If your program requires job related information, you must pass this information as arguments. Do not include environment variables, such as %system32%, in <i>pProgram</i> or <i>pParameters</i> — they are not expanded.

You should include the full path to the program. If any of the arguments in <i>pParameters</i> include a path that uses long file names, such as the module name, use quotes around the path.

If the program you want to execute uses the reply or download file, the program must call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method to make the files available to the client.

Call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a> method to specify when to execute the program. You can request command line execution only for job error or transferred events, not job modification events. Note that BITS still executes the command line even if you call the 
<b>SetNotifyCmdLine</b> method after the event occurs.

If the BITS job is in a service account context (ie, networkservice/localsystem/localservice), no form of command-line callback will execute. 

If you call both the <b>SetNotifyCmdLine</b> method 
and the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method, BITS will execute the command line only if the notification interface becomes invalid or the notification method that BITS calls returns a failure  code. For example, if the notification method that BITS calls returns a E_FAIL, BITS will execute the command line. However, if the notification method returns <b>S_OK</b>, BITS will not execute the command line. If the  notification method and command line execution request both fail, BITS will send the notification again after the minimum retry period expires. 

Note that calling the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-takeownership">IBackgroundCopyJob::TakeOwnership</a> method removes command line notification from the job.


#### Examples

For an example that calls the 
<b>SetNotifyCmdLine</b> method, see 
<a href="/windows/desktop/Bits/registering-to-execute-a-program">Registering to Execute a Program</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getnotifycmdline">IBackgroundCopyJob2::GetNotifyCmdLine</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>