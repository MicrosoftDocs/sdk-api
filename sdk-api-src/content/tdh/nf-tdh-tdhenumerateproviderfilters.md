---
UID: NF:tdh.TdhEnumerateProviderFilters
title: TdhEnumerateProviderFilters function
author: windows-sdk-content
description: Enumerates the filters that the specified provider defined in the manifest.
old-location: etw\tdhenumerateproviderfilters.htm
old-project: etw
ms.assetid: bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TdhEnumerateProviderFilters, TdhEnumerateProviderFilters function [ETW], etw.tdhenumerateproviderfilters, tdh/TdhEnumerateProviderFilters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: TEMPLATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhEnumerateProviderFilters
product: Windows
targetos: Windows
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TdhEnumerateProviderFilters function


## -description


The <b>TdhEnumerateProviderFilters</b> function enumerates the filters that the specified provider defined in the manifest.


## -parameters




### -param Guid

TBD


### -param TdhContextCount [in]

Not used.


### -param TdhContext

TBD


### -param FilterCount [in]

The number of filter structures that the <i>pBuffer</i> buffer contains. Is zero if the <i>pBuffer</i> buffer is insufficient.


### -param Buffer

TBD


### -param BufferSize

TBD




#### - pBuffer [out, optional]

User-allocated buffer to receive the filter information. For details, see the <a href="https://msdn.microsoft.com/0541b24a-8531-4828-8c3b-d889e58b0b38">PROVIDER_FILTER_INFO</a> structure.


#### - pBufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.


#### - pGuid [in]

GUID that identifies the provider whose filters you want to retrieve.


#### - pTdhContext [in, optional]

Not used.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pBuffer</i> buffer is too small. Use the required buffer size set in <i>pBufferSize</i> to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema for the event was not found.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>resourceFileName</b> attribute in the manifest contains the location of the provider binary. When you register the manifest, the location is written to the registry. TDH was unable to find the binary based on the registered location.

</td>
</tr>
</table>
 




## -remarks



This function uses the XML manifest to retrieve the information.



