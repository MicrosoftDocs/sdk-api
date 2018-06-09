---
UID: NF:ntmsapi.DeallocateNtmsMedia
title: DeallocateNtmsMedia function
author: windows-sdk-content
description: The DeallocateNtmsMedia function deallocates the side associated with the specified logical media.
old-location: fs\deallocatentmsmedia.htm
old-project: Rsm
ms.assetid: e053c725-2da6-4eeb-b471-644847dd8db5
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: DeallocateNtmsMedia, DeallocateNtmsMedia function [Files], _zaw_deallocatentmsmedia, base.deallocatentmsmedia, fs.deallocatentmsmedia, ntmsapi/DeallocateNtmsMedia
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
 - DeallocateNtmsMedia
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DeallocateNtmsMedia function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeallocateNtmsMedia</b> function deallocates the side associated with the specified logical media.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaId [in]

Unique identifier of the logical media (LMID).


### -param dwOptions

Reserved; must be zero.


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
NTMS_CONTROL_ACCESS to the media's media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_MODIFY_ACCESS to the media's media pool is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
The session handle missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The LMID is not valid.

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
<dt><b>ERROR_INVALID_PARTITION</b></dt>
</dl>
</td>
<td width="60%">
The LMID side is not valid.

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



When a logical medium is deallocated with the 
<b>DeallocateNtmsMedia</b> function, RSM puts the side associated with the logical media in the Available or Decommissioned media state. The logical media is deleted from the system when the logical media is deallocated.

Sides are decommissioned upon deallocation if the side has been allocated the maximum number of times specified in the media pool. After media is in the Decommissioned state, it cannot be allocated again.

<b>Windows Server 2003:  </b>If media is being returned to the free pool, NTMS_USE_ACCESS to the free pool and NTMS_CONTROL_ACCESS to the source pool is required. If the free pool is not the destination media pool, NTMS_CONTROL_ACCESS is required on both source and destination pools.




## -see-also




<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a>



<a href="https://www.bing.com/search?q=Media+Services+Functions">Media Services Functions</a>
 

 

