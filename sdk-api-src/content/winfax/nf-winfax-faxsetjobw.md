---
UID: NF:winfax.FaxSetJobW
title: FaxSetJobW function (winfax.h)
author: windows-sdk-content
description: A fax client application calls the FaxSetJob function to pause, resume, cancel, or restart a specified fax job.
old-location: fax\_mfax_faxsetjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4pwi.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaxSetJob, FaxSetJob function [Fax Service], FaxSetJobA, FaxSetJobW, JC_DELETE, JC_PAUSE, JC_RESTART, JC_RESUME, _mfax_faxsetjob, fax._mfax_faxsetjob, winfax/FaxSetJob, winfax/FaxSetJobA, winfax/FaxSetJobW
ms.topic: function
f1_keywords:
- winfax/FaxSetJob
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetJobW (Unicode) and FaxSetJobA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- WinFax.lib
- WinFax.dll
api_name:
- FaxSetJob
- FaxSetJobA
- FaxSetJobW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxSetJobW function


## -description


A fax client application calls the <b>FaxSetJob</b> function to pause, resume, cancel, or restart a specified fax job.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.


### -param JobId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a unique number to identify the fax job to modify. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a> function to retrieve a valid fax job identifier to use in the <i>JobId</i> parameter.


### -param Command [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the job command to perform. This parameter can be one of the following values.



#### JC_DELETE

Cancel the specified fax job. The job can be active or queued.



#### JC_PAUSE

Pause the specified queued fax job. If the fax job is active, the fax service pauses the job when it returns to the queued state.



#### JC_RESUME

Resume the paused fax job.



#### JC_RESTART

Restart the specified fax job.


### -param JobEntry [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a>*</b>

Not used, must be <b>NULL</b>.


##### - Command.JC_DELETE

Cancel the specified fax job. The job can be active or queued.


##### - Command.JC_PAUSE

Pause the specified queued fax job. If the fax job is active, the fax service pauses the job when it returns to the queued state.


##### - Command.JC_RESTART

Restart the specified fax job.


##### - Command.JC_RESUME

Resume the paused fax job.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_JOB_MANAGE</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is <b>NULL</b>, or one or all of the <i>Command</i>, <i>JobEntry</i>, or <i>JobId</i> parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



An application typically calls the <b>FaxSetJob</b> function to manage a queued fax job. To terminate a fax transmission that is in progress, an application can call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxabort">FaxAbort</a> function.

For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-modifying-a-fax-job">Modifying a Fax Job</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-terminating-a-fax-job">Terminating a Fax Job</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_job_entrya">FAX_JOB_ENTRY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxabort">FaxAbort</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetjoba">FaxGetJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>
 

 

