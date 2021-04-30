---
UID: NF:ntmsapi.CancelNtmsOperatorRequest
title: CancelNtmsOperatorRequest function (ntmsapi.h)
description: The CancelNtmsOperatorRequest function cancels the specified RSM operator request.
helpviewer_keywords: ["CancelNtmsOperatorRequest","CancelNtmsOperatorRequest function [Files]","_zaw_cancelntmsoperatorrequest","base.cancelntmsoperatorrequest","fs.cancelntmsoperatorrequest","ntmsapi/CancelNtmsOperatorRequest"]
old-location: fs\cancelntmsoperatorrequest.htm
tech.root: fs
ms.assetid: d0ba65fe-0355-4bd6-b9ad-98e8f7992827
ms.date: 12/05/2018
ms.keywords: CancelNtmsOperatorRequest, CancelNtmsOperatorRequest function [Files], _zaw_cancelntmsoperatorrequest, base.cancelntmsoperatorrequest, fs.cancelntmsoperatorrequest, ntmsapi/CancelNtmsOperatorRequest
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
 - CancelNtmsOperatorRequest
 - ntmsapi/CancelNtmsOperatorRequest
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
 - CancelNtmsOperatorRequest
---

# CancelNtmsOperatorRequest function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CancelNtmsOperatorRequest</b> function cancels the specified RSM operator request.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpRequestId [in]

Unique identifier of the operator request to be canceled. 




To retrieve the list of existing operator requests, use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a> function. You can also use the identifier returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a> function.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user that tried to execute this function does not have administrator privileges. Only an administrator of the RSM server can cancel operator requests.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The request identifier is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The request has already been completed or canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operator request object ID was not found. This error can occur if the request ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been canceled.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Operator Request Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-satisfyntmsoperatorrequest">SatisfyNtmsOperatorRequest</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a>