---
UID: NF:ntmsapi.ChangeNtmsMediaType
title: ChangeNtmsMediaType function
author: windows-sdk-content
description: The ChangeNtmsMediaType function moves the specified PMID to the specified target media pool and sets the PMID's media type identifier to the media type of the target media pool.
old-location: fs\changentmsmediatype.htm
tech.root: Rsm
ms.assetid: 89b3eb9b-0614-47a9-825e-1335c7fc5d0d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ChangeNtmsMediaType, ChangeNtmsMediaType function [Files], _zaw_changentmsmediatype, base.changentmsmediatype, fs.changentmsmediatype, ntmsapi/ChangeNtmsMediaType
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
 - ChangeNtmsMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChangeNtmsMediaType function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ChangeNtmsMediaType</b> function moves the specified PMID to the specified target media pool and sets the PMID's media type identifier to the media type of the target media pool.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaId [in]

Unique identifier of the physical media to be moved.


### -param lpPoolId [in]

Unique identifier of the media pool from which the media is to be allocated.


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
NTMS_MODIFY_ACCESS to the computer or the media's media pool is denied. Other security errors are possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b> NTMS_MODIFY_ACCESS to the media's media pool is denied.

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
The media pool or media ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

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
</table>
 




## -remarks



The 
<b>ChangeNtmsMediaType</b> function uses the same policy for moving media as the 
<a href="https://msdn.microsoft.com/6bc11877-6657-4e8b-8239-bb2720cfb256">MoveToNtmsMediaPool</a> function (unrecognized media can only be moved to the free pool).




## -see-also




<a href="https://msdn.microsoft.com/fa8ad4af-eeb8-445e-ac6c-671badb651ec">AddNtmsMediaType</a>



<a href="https://msdn.microsoft.com/c2a2bc8a-4230-44c4-b6bc-4b4e2a9fece1">DeleteNtmsMediaType</a>



<a href="removable_storage_manager_functions.htm">Media Services Functions</a>
 

 

