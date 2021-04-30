---
UID: NF:tdh.TdhEnumerateProviderFilters
title: TdhEnumerateProviderFilters function (tdh.h)
description: Enumerates the filters that the specified provider defined in the manifest.
helpviewer_keywords: ["TdhEnumerateProviderFilters","TdhEnumerateProviderFilters function [ETW]","etw.tdhenumerateproviderfilters","tdh/TdhEnumerateProviderFilters"]
old-location: etw\tdhenumerateproviderfilters.htm
tech.root: ETW
ms.assetid: bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b
ms.date: 12/05/2018
ms.keywords: TdhEnumerateProviderFilters, TdhEnumerateProviderFilters function [ETW], etw.tdhenumerateproviderfilters, tdh/TdhEnumerateProviderFilters
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
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhEnumerateProviderFilters
 - tdh/TdhEnumerateProviderFilters
dev_langs:
 - c++
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
---

# TdhEnumerateProviderFilters function


## -description

The <b>TdhEnumerateProviderFilters</b> function enumerates the filters that the specified provider defined in the manifest.

## -parameters

### -param Guid [in]

GUID that identifies the provider whose filters you want to retrieve.

### -param TdhContextCount [in]

Not used.

### -param TdhContext [in, optional]

Not used.

### -param FilterCount [in]

The number of filter structures that the <i>pBuffer</i> buffer contains. Is zero if the <i>pBuffer</i> buffer is insufficient.

### -param Buffer [out, optional]

User-allocated buffer to receive the filter information. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-provider_filter_info">PROVIDER_FILTER_INFO</a> structure.

### -param BufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

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