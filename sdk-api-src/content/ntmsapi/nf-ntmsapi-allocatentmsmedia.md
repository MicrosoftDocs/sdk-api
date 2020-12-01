---
UID: NF:ntmsapi.AllocateNtmsMedia
title: AllocateNtmsMedia function (ntmsapi.h)
description: The AllocateNtmsMedia function allocates a piece of available media.
helpviewer_keywords: ["AllocateNtmsMedia","AllocateNtmsMedia function [Files]","NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE","NTMS_ALLOCATE_NEW","NTMS_ALLOCATE_NEXT","_zaw_allocatentmsmedia","base.allocatentmsmedia","fs.allocatentmsmedia","ntmsapi/AllocateNtmsMedia"]
old-location: fs\allocatentmsmedia.htm
tech.root: fs
ms.assetid: a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600
ms.date: 12/05/2018
ms.keywords: AllocateNtmsMedia, AllocateNtmsMedia function [Files], NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE, NTMS_ALLOCATE_NEW, NTMS_ALLOCATE_NEXT, _zaw_allocatentmsmedia, base.allocatentmsmedia, fs.allocatentmsmedia, ntmsapi/AllocateNtmsMedia
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
 - AllocateNtmsMedia
 - ntmsapi/AllocateNtmsMedia
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
 - AllocateNtmsMedia
---

# AllocateNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available for use as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>AllocateNtmsMedia</b> function allocates a piece of available media.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpMediaPool [in]

Unique identifier of the media pool from which the media is to be allocated. Only application pools may be specified for allocation.

### -param lpPartition [in]

Part identifier of a side to use as a logical media identifier (LMID). The side must be in the Available or Import state. This feature can be used to allocate a particular side or to import media. This parameter is optional.

### -param lpMediaId [out]

LMID of the allocated medium. This parameter is <b>NULL</b> if the medium cannot be allocated.

### -param dwOptions [in]

Options. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE"></a><a id="ntms_allocate_error_if_unavailable"></a><dl>
<dt><b>NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
Prevents the submission of an operator request for new media if none can be allocated with the specified constraints.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_ALLOCATE_NEW"></a><a id="ntms_allocate_new"></a><dl>
<dt><b>NTMS_ALLOCATE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Allocates a side of the specified medium that cannot be shared with another application's logical media. For example, this value reserves the second side of two-sided optical media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_ALLOCATE_NEXT"></a><a id="ntms_allocate_next"></a><dl>
<dt><b>NTMS_ALLOCATE_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Allocate the next side of the multi-sided medium previously allocated with the NTMS_ALLOCATE_NEW value. This allows a single application to use both sides of a piece of two-sided media and ensure that the application owns all the data on the piece of physical media. 




If all the sides of the medium are already allocated, the allocation request fails.

</td>
</tr>
</table>

### -param dwTimeout [in]

Maximum time allowed to allocate the specified media, in milliseconds. If this parameter is INFINITE, the function will not time out. If this parameter is zero, it will wait for media. Note that this function does not queue a request for more media if the <i>dwOptions</i> parameter specifies NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE.

### -param lpAllocateInformation [out]

Pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_allocation_information">NTMS_ALLOCATION_INFORMATION</a> structure that receives the source media pool from which the medium was taken. This parameter can be <b>NULL</b>.

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
NTMS_CONTROL_ACCESS to the media's media pool is denied. Other security error are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_MODIFY_ACCESS to media's media pool is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operator canceled the request for new media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
An intermediate resource is not available; for example, the free media pool is not available.

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
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The partition ID or LMID was not valid upon input when using the NTMS_ALLOCATE_NEXT flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The media pool ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media or media pool ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The specified media is offline and cannot be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No media has been allocated within the specified time-out event.

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
The time-out event expired before media was available.

</td>
</tr>
</table>

## -remarks

The 
<b>AllocateNtmsMedia</b> function returns an LMID. Depending upon the media pool's policy, if the specified media pool does not contain any online Available media, 
<b>AllocateNtmsMedia</b> might search the free media pool for the specified medium to move to the specified media pool. Media from the designated media pool is allocated first, and then the free media is moved and allocated.

If the media pool contains any online Available media, a medium from the pool is allocated.

If the media pool is configured to allocate media from the free pool automatically, and the free pool contains online Available media, a medium is moved to the specified pool and allocated.

<b>Windows Server 2003:  </b>If media is being allocated from the free pool, NTMS_USE_ACCESS to the free pool and NTMS_CONTROL_ACCESS to the destination pool is required. If the free pool is not the source media pool, NTMS_CONTROL_ACCESS is required on both source and destination pools.

When the NTMS_ALLOCATE_NEXT value is specified, the <i>lpMediaId</i> parameter must point to a valid media ID at the time of invocation. In this case, <i>lpMediaId</i> is used as an IN and OUT parameter. The next side of the multiple sided medium specified by <i>lpMediaId</i> is allocated, and the new partition ID is returned through <i>lpMediaId</i> (overwriting the original media ID passed in).

If NTMS_ALLOCATE_ERROR_IF_UNAVAILABLE is specified, ERROR_MEDIA_ UNAVAILABLE is returned if no media is available.

When necessary, RSM generates an operator request to insert new or Available media. If the time specified in the <i>dwTimeout</i> parameter elapses before the operator request is handled, RSM returns ERROR_TIMEOUT and deletes the operator request.

If the user cancels the allocation request, RSM returns ERROR_CANCELLED.

If a user indicates that the operator request has been satisfied, the request is deleted and RSM retries the process.

When an application requires new media containing data, a user or administrator places the media in a library or drive. RSM identifies the media and places it in the import pool. The application searches the import pool, moves the media to its application pool and allocates it. This routine process can be streamlined and made atomic through a single call to 
<b>AllocateNtmsMedia</b>. After searching the import pool the application can call 
<b>AllocateNtmsMedia</b>, passing the partition ID of the side as the value of the <i>lpPartId</i> parameter. RSM then:

<ol>
<li>moves the medium to the specified media pool.</li>
<li>changes the media's state to allocated.</li>
<li>returns an LMID.</li>
</ol>
<div class="alert"><b>Note</b>  For two-sided media, the flip side remains in the Import state and is not available for use until imported.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-deallocatentmsmedia">DeallocateNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>



<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_allocation_information">NTMS_ALLOCATION_INFORMATION</a>