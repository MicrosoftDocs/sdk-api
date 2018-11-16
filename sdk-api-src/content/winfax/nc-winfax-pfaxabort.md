---
UID: NC:winfax.PFAXABORT
title: PFAXABORT
author: windows-sdk-content
description: A fax client application calls the FaxAbort function to terminate a fax job.
old-location: fax\_mfax_faxabort.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_03jo.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FaxAbortA, FaxAbortW, PFAXABORT, PFAXABORT callback, PFAXABORT callback function [Fax Service], _mfax_faxabort, fax._mfax_faxabort, winfax/FaxAbortA, winfax/FaxAbortW, winfax/PFAXABORT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxAbortW (Unicode) and FaxAbortA (ANSI)
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
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAXABORT
 - FaxAbortA
 - FaxAbortW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXABORT callback function


## -description


A fax client application calls the <b>FaxAbort</b> function to terminate a fax job.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job to terminate.


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
Access is denied. You must own the job, or have <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_JOB_MANAGE</a> access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>JobId</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



An application typically calls the <b>FaxAbort</b> function to terminate a fax transmission that is in progress. To manage a queued fax job, an application typically calls the <a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a> function. <b>FaxSetJob</b> can cancel an active job; the function can also pause, resume, cancel, or restart a queued fax job.

Call the <a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a> function to retrieve a valid value to use in the <i>JobId</i> parameter.

For more information, see <a href="https://msdn.microsoft.com/8bcfa999-85d8-43f1-a7f1-59d5a824376a">Modifying a Fax Job</a> and <a href="https://msdn.microsoft.com/b957ed68-3e48-4c97-8c7c-3329a52f41bb">Terminating a Fax Job</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/bbf8def4-4af0-4315-94f9-860f9db1eefa">FaxSendDocument</a>



<a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a>



<a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a>
 

 

