---
UID: NF:ntmsapi.WaitForNtmsOperatorRequest
title: WaitForNtmsOperatorRequest function (ntmsapi.h)
description: The WaitForNtmsOperatorRequest function waits for the specified RSM operator request.
helpviewer_keywords: ["WaitForNtmsOperatorRequest","WaitForNtmsOperatorRequest function [Files]","_zaw_waitforntmsoperatorrequest","base.waitforntmsoperatorrequest","fs.waitforntmsoperatorrequest","ntmsapi/WaitForNtmsOperatorRequest"]
old-location: fs\waitforntmsoperatorrequest.htm
tech.root: fs
ms.assetid: abc78047-a6d7-4e98-baec-5e4ba394c64f
ms.date: 12/05/2018
ms.keywords: WaitForNtmsOperatorRequest, WaitForNtmsOperatorRequest function [Files], _zaw_waitforntmsoperatorrequest, base.waitforntmsoperatorrequest, fs.waitforntmsoperatorrequest, ntmsapi/WaitForNtmsOperatorRequest
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WaitForNtmsOperatorRequest
 - ntmsapi/WaitForNtmsOperatorRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - WaitForNtmsOperatorRequest
---

# WaitForNtmsOperatorRequest function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>WaitForNtmsOperatorRequest</b> function waits for the specified RSM operator request.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpRequestId [in]

Operator request identifier created by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a> function.

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
<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a> if RSM returns this error.

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
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a> function to submit operator requests and use the 
<b>WaitForNtmsOperatorRequest</b> function to wait for their resolution.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cancelntmsoperatorrequest">CancelNtmsOperatorRequest</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Operator Request Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-satisfyntmsoperatorrequest">SatisfyNtmsOperatorRequest</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a>