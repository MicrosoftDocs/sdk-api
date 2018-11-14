---
UID: NF:ntmsapi.CancelNtmsLibraryRequest
title: CancelNtmsLibraryRequest function
author: windows-sdk-content
description: The CancelNtmsLibraryRequest function cancels outstanding RSM requests, such as calls to the CleanNtmsDrive function. If the library is busy, RSM queues the cancellation and returns success.
old-location: fs\cancelntmslibraryrequest.htm
tech.root: Rsm
ms.assetid: 99626e6f-2716-4e36-b4ec-3fef0315ea41
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CancelNtmsLibraryRequest, CancelNtmsLibraryRequest function [Files], _zaw_cancelntmslibraryrequest, base.cancelntmslibraryrequest, fs.cancelntmslibraryrequest, ntmsapi/CancelNtmsLibraryRequest
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - CancelNtmsLibraryRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CancelNtmsLibraryRequest
: 
---

# CancelNtmsLibraryRequest function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CancelNtmsLibraryRequest</b> function cancels outstanding RSM requests, such as calls to the 
<a href="https://msdn.microsoft.com/55a8e7c0-85fd-40c5-b5b9-46ad321761c4">CleanNtmsDrive</a> function. If the library is busy, RSM queues the cancellation and returns success.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpRequestId [in]

Unique identifier of the library request to be canceled. 




To retrieve the list of existing library requests, use the 
<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a> function.


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




<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Library Control Functions</a>
 

 

