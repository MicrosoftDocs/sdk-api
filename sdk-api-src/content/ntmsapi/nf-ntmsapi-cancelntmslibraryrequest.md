---
UID: NF:ntmsapi.CancelNtmsLibraryRequest
title: CancelNtmsLibraryRequest function (ntmsapi.h)
description: The CancelNtmsLibraryRequest function cancels outstanding RSM requests, such as calls to the CleanNtmsDrive function. If the library is busy, RSM queues the cancellation and returns success.
helpviewer_keywords: ["CancelNtmsLibraryRequest","CancelNtmsLibraryRequest function [Files]","_zaw_cancelntmslibraryrequest","base.cancelntmslibraryrequest","fs.cancelntmslibraryrequest","ntmsapi/CancelNtmsLibraryRequest"]
old-location: fs\cancelntmslibraryrequest.htm
tech.root: fs
ms.assetid: 99626e6f-2716-4e36-b4ec-3fef0315ea41
ms.date: 12/05/2018
ms.keywords: CancelNtmsLibraryRequest, CancelNtmsLibraryRequest function [Files], _zaw_cancelntmslibraryrequest, base.cancelntmslibraryrequest, fs.cancelntmslibraryrequest, ntmsapi/CancelNtmsLibraryRequest
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
 - CancelNtmsLibraryRequest
 - ntmsapi/CancelNtmsLibraryRequest
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
 - CancelNtmsLibraryRequest
---

# CancelNtmsLibraryRequest function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CancelNtmsLibraryRequest</b> function cancels outstanding RSM requests, such as calls to the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cleanntmsdrive">CleanNtmsDrive</a> function. If the library is busy, RSM queues the cancellation and returns success.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpRequestId [in]

Unique identifier of the library request to be canceled. 




To retrieve the list of existing library requests, use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a> function.

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
Only an administrator of the RSM server can cancel library requests. This error is also returned if the request is currently being handled and cannot be deleted.

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
There was an allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The library request object ID was not found. This error occurs if the request is completed prior to issuing the cancel or when a request ID that is not valid is specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The library request has been queued for cancellation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>