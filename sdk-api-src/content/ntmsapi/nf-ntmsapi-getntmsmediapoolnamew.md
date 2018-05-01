---
UID: NF:ntmsapi.GetNtmsMediaPoolNameW
title: GetNtmsMediaPoolNameW function
author: windows-driver-content
description: The GetNtmsMediaPoolName function retrieves the specified media pool's full name hierarchy.
old-location: fs\getntmsmediapoolname.htm
old-project: Rsm
ms.assetid: 72b9028b-d97e-4441-8677-1a4a0b03dee2
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetNtmsMediaPoolName, GetNtmsMediaPoolName function [Files], GetNtmsMediaPoolNameA, GetNtmsMediaPoolNameW, _zaw_getntmsmediapoolname, base.getntmsmediapoolname, fs.getntmsmediapoolname, ntmsapi/GetNtmsMediaPoolName, ntmsapi/GetNtmsMediaPoolNameA, ntmsapi/GetNtmsMediaPoolNameW
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
req.unicode-ansi: GetNtmsMediaPoolNameW (Unicode) and GetNtmsMediaPoolNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntmsapi.dll
api_name:
-	GetNtmsMediaPoolName
-	GetNtmsMediaPoolNameA
-	GetNtmsMediaPoolNameW
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# GetNtmsMediaPoolNameW function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsMediaPoolName</b> function retrieves the specified media pool's full name hierarchy.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpPoolId [in]

Unique identifier of the media pool whose name is to be retrieved.


### -param lpNameBuf

TBD


### -param lpdwBufSize [in, out]

Size of the <i>lpBufName</i> buffer, on input. On output, the number of characters in the full name hierarchy.


#### - lpBufName [out]

Pointer to a buffer that receives the name of the media pool.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size is not large enough. The correct size is returned in <i>lpdwBufSize</i>.

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
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The media pool ID is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory allocation failed.

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
 




## -see-also




<a href="https://msdn.microsoft.com/a55a8952-2b64-4082-9422-31484c7e777f">CreateNtmsMediaPool</a>



<a href="removable_storage_manager_functions.htm">Media Services Functions</a>
 

 

