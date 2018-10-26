---
UID: NF:ntmsapi.DecommissionNtmsMedia
title: DecommissionNtmsMedia function
author: windows-sdk-content
description: The DecommissionNtmsMedia function moves a side from the Available state to the Decommissioned state.
old-location: fs\decommissionntmsmedia.htm
tech.root: Rsm
ms.assetid: 2bb1a54b-6308-4ccd-9fc6-1b11f4432a3f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DecommissionNtmsMedia, DecommissionNtmsMedia function [Files], _zaw_decommissionntmsmedia, base.decommissionntmsmedia, fs.decommissionntmsmedia, ntmsapi/DecommissionNtmsMedia
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
 - DecommissionNtmsMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DecommissionNtmsMedia function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DecommissionNtmsMedia</b> function moves a side from the Available state to the Decommissioned state.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaId [in]

Unique identifier of a side of a piece of physical media.


## -returns



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
The media identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The media pool for media is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media identifier is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The media is not in the Available state.

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



Media decommissioned by the 
<b>DecommissionNtmsMedia</b> function is recognized by RSM but the decommissioned media does not contain any data and is never again used.

Only media that is in the Available state can be decommissioned. For more information, see 
<a href="https://msdn.microsoft.com/231e80c5-5ea1-4f17-adf7-83d97abe35c8">Media Life Cycle</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Media Services Functions</a>
 

 

