---
UID: NF:winfax.FaxSetJobA
title: FaxSetJobA function
author: windows-sdk-content
description: A fax client application calls the FaxSetJob function to pause, resume, cancel, or restart a specified fax job.
old-location: fax\_mfax_faxsetjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4pwi.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FaxSetJob, FaxSetJob function [Fax Service], FaxSetJobA, FaxSetJobW, JC_DELETE, JC_PAUSE, JC_RESTART, JC_RESUME, _mfax_faxsetjob, fax._mfax_faxsetjob, winfax/FaxSetJob, winfax/FaxSetJobA, winfax/FaxSetJobW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
- apiref
: 
- 
: 
- FaxSetJobA
: 
---

# FaxSetJobA function


## -description


A fax client application calls the <b>FaxSetJob</b> function to pause, resume, cancel, or restart a specified fax job.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param JobId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a unique number to identify the fax job to modify. Call the <a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a> function to retrieve a valid fax job identifier to use in the <i>JobId</i> parameter.


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

Type: <b>const <a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a>*</b>

Not used, must be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

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
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_JOB_MANAGE</a> access is required.

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



An application typically calls the <b>FaxSetJob</b> function to manage a queued fax job. To terminate a fax transmission that is in progress, an application can call the <a href="https://msdn.microsoft.com/63c0f193-5e54-4273-9b6a-cc777523550e">FaxAbort</a> function.

For more information, see <a href="https://msdn.microsoft.com/8bcfa999-85d8-43f1-a7f1-59d5a824376a">Modifying a Fax Job</a> and <a href="https://msdn.microsoft.com/b957ed68-3e48-4c97-8c7c-3329a52f41bb">Terminating a Fax Job</a>.




## -see-also




<a href="https://msdn.microsoft.com/7e75f960-9a8a-4453-bb56-1dc80d5cadcc">FAX_JOB_ENTRY</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/63c0f193-5e54-4273-9b6a-cc777523550e">FaxAbort</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/784c4945-b4cc-446b-b0d4-c2fc58d46a9d">FaxGetJob</a>



<a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a>



<a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a>
 

 

