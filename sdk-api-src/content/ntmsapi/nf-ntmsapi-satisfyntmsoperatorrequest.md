---
UID: NF:ntmsapi.SatisfyNtmsOperatorRequest
title: SatisfyNtmsOperatorRequest function (ntmsapi.h)
description: The SatisfyNtmsOperatorRequest function completes the specified RSM operator request.
helpviewer_keywords: ["SatisfyNtmsOperatorRequest","SatisfyNtmsOperatorRequest function [Files]","_zaw_satisfyntmsoperatorrequest","base.satisfyntmsoperatorrequest","fs.satisfyntmsoperatorrequest","ntmsapi/SatisfyNtmsOperatorRequest"]
old-location: fs\satisfyntmsoperatorrequest.htm
tech.root: fs
ms.assetid: 37f9c9c4-7fb2-4559-94a4-e508b277e69e
ms.date: 12/05/2018
ms.keywords: SatisfyNtmsOperatorRequest, SatisfyNtmsOperatorRequest function [Files], _zaw_satisfyntmsoperatorrequest, base.satisfyntmsoperatorrequest, fs.satisfyntmsoperatorrequest, ntmsapi/SatisfyNtmsOperatorRequest
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
 - SatisfyNtmsOperatorRequest
 - ntmsapi/SatisfyNtmsOperatorRequest
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
 - SatisfyNtmsOperatorRequest
---

# SatisfyNtmsOperatorRequest function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SatisfyNtmsOperatorRequest</b> function completes the specified RSM operator request.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpRequestId [in]

Operator request object ID. This value is returned by 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a>.

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
The user that tried to execute this function does not have administrator privileges. Only an administrator of the RSM server can satisfy operator requests.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operator request object ID was not found. This error occurs if the request is completed before the operation has been satisfied or when a request ID that is not valid is specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been satisfied.

</td>
</tr>
</table>

## -remarks

If an application detects that the operator did not acknowledge a satisfied operator request, the application can use the 
<b>SatisfyNtmsOperatorRequest</b> function to remove the request.

For a list of the existing operator requests to cancel with the 
<b>SatisfyNtmsOperatorRequest</b> function, see the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a> function.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cancelntmsoperatorrequest">CancelNtmsOperatorRequest</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Operator Request Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-submitntmsoperatorrequesta">SubmitNtmsOperatorRequest</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsoperatorrequest">WaitForNtmsOperatorRequest</a>