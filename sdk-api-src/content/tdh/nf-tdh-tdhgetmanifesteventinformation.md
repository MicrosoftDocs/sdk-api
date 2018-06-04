---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TdhGetManifestEventInformation function


## -description


The <b>TdhGetManifestEventInformation</b> function retrieves metadata about an event in  a manifest.


## -parameters




### -param ProviderGuid [in]

A GUID that identifies the manifest provider whose event metadata you want to retrieve. 


### -param EventDescriptor [in]

A pointer to the event descriptor that contains information such as event id, version, op-code, and keyword. For details, see the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure


### -param Buffer [out]

A user-allocated buffer to receive the metadata about an event in  a provider manifest. For details, see the <a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a> structure.


### -param BufferSize [in, out]

The size, in bytes, of the buffer pointed to by the <i>Buffer</i> parameter. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns <b>ERROR_INSUFFICIENT_BUFFER</b> and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
There are no events defined for the provider GUID in the manifest.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The metadata for the provider was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the buffer pointed to by the <i>Buffer</i> parameter is too small. Use the required buffer size set in the <i>BufferSize</i> parameter to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema information for supplied provider GUID was not found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/CC392841-7436-4543-A846-FB5A27D9A014">PROVIDER_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/93A03E1D-4047-49F1-987B-FB7BE03E0483">TdhEnumerateManifestProviderEvents</a>
 

 

