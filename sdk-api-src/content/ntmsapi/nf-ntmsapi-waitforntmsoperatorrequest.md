---
UID: NF:ntmsapi.WaitForNtmsOperatorRequest
title: WaitForNtmsOperatorRequest function
author: windows-sdk-content
description: The WaitForNtmsOperatorRequest function waits for the specified RSM operator request.
old-location: fs\waitforntmsoperatorrequest.htm
old-project: Rsm
ms.assetid: abc78047-a6d7-4e98-baec-5e4ba394c64f
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: WaitForNtmsOperatorRequest, WaitForNtmsOperatorRequest function [Files], _zaw_waitforntmsoperatorrequest, base.waitforntmsoperatorrequest, fs.waitforntmsoperatorrequest, ntmsapi/WaitForNtmsOperatorRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - WaitForNtmsOperatorRequest
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# WaitForNtmsOperatorRequest function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>WaitForNtmsOperatorRequest</b> function waits for the specified RSM operator request.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpRequestId [in]

Operator request identifier created by the 
<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a> function.


### -param dwTimeout [in]

Number of milliseconds to wait. To check for an operator request, pass a time-out value of zero. If you specify a value of INFINITE, this function does not time-out.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operator request was canceled by an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
 One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the operator request object. Object requests are flushed from the database. Application should call a function like 
<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a> if RSM returns this error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time specified in the <i>dwTimeout</i> parameter elapsed before the completion of the operator request.

</td>
</tr>
</table>
 




## -remarks



Operator requests specified with the 
<b>WaitForNtmsOperatorRequest</b> function are used to request media, to request that the medium be moved from one library to another, or to request RSM device service.

An application uses 
<b>WaitForNtmsOperatorRequest</b> to wait for resolution of an operator request. The request can be satisfied, rejected, deleted, or timed out.

Typically, applications use the 
<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a> function to submit operator requests and use the 
<b>WaitForNtmsOperatorRequest</b> function to wait for their resolution.




## -see-also




<a href="https://msdn.microsoft.com/d0ba65fe-0355-4bd6-b9ad-98e8f7992827">CancelNtmsOperatorRequest</a>



<a href="removable_storage_manager_functions.htm">Operator Request Functions</a>



<a href="https://msdn.microsoft.com/37f9c9c4-7fb2-4559-94a4-e508b277e69e">SatisfyNtmsOperatorRequest</a>



<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a>
 

 

