---
UID: NF:ntmsapi.DeleteNtmsRequests
title: DeleteNtmsRequests function (ntmsapi.h)
description: The DeleteNtmsRequests function deletes a request or a list of requests from the RSM database.
helpviewer_keywords: ["DeleteNtmsRequests","DeleteNtmsRequests function [Files]","NTMS_LIBREQUEST","NTMS_OPREQUEST","_zaw_deletentmsrequests","base.deletentmsrequests","fs.deletentmsrequests","ntmsapi/DeleteNtmsRequests"]
old-location: fs\deletentmsrequests.htm
tech.root: fs
ms.assetid: 5368184a-419c-4cb7-b27f-b55fc26b4e81
ms.date: 12/05/2018
ms.keywords: DeleteNtmsRequests, DeleteNtmsRequests function [Files], NTMS_LIBREQUEST, NTMS_OPREQUEST, _zaw_deletentmsrequests, base.deletentmsrequests, fs.deletentmsrequests, ntmsapi/DeleteNtmsRequests
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
 - DeleteNtmsRequests
 - ntmsapi/DeleteNtmsRequests
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
 - DeleteNtmsRequests
---

# DeleteNtmsRequests function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeleteNtmsRequests</b> function deletes a request or a list of requests from the RSM database. Library or operator requests that are in a completed, failed, refused, or canceled state are removed. Submitted requests, queued requests, waiting requests, and in progress requests cannot be deleted.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpRequestId [in]

List of identifiers of the library and operator requests to be deleted.

### -param dwType [in]

Request type. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LIBREQUEST"></a><a id="ntms_librequest"></a><dl>
<dt><b>NTMS_LIBREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Library request.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPREQUEST"></a><a id="ntms_oprequest"></a><dl>
<dt><b>NTMS_OPREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Operator request.

</td>
</tr>
</table>

### -param dwCount [in]

Number of requests in the list.

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
NTMS_MODIFY_ACCESS to the computer is denied. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the computer is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The type identifier is not valid.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function executed successfully.

</td>
</tr>
</table>

## -remarks

An error is not returned if a request or list of requests is not found.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>