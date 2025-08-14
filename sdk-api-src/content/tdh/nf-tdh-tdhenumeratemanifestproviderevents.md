---
UID: NF:tdh.TdhEnumerateManifestProviderEvents
title: TdhEnumerateManifestProviderEvents function (tdh.h)
description: Retrieves the list of events present in the provider manifest.
helpviewer_keywords: ["TdhEnumerateManifestProviderEvents","TdhEnumerateManifestProviderEvents function [ETW]","etw.tdhenumeratemanifestproviderevents","tdh/TdhEnumerateManifestProviderEvents"]
old-location: etw\tdhenumeratemanifestproviderevents.htm
tech.root: ETW
ms.assetid: 93A03E1D-4047-49F1-987B-FB7BE03E0483
ms.date: 12/05/2018
ms.keywords: TdhEnumerateManifestProviderEvents, TdhEnumerateManifestProviderEvents function [ETW], etw.tdhenumeratemanifestproviderevents, tdh/TdhEnumerateManifestProviderEvents
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - TdhEnumerateManifestProviderEvents
 - tdh/TdhEnumerateManifestProviderEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhEnumerateManifestProviderEvents
---

# TdhEnumerateManifestProviderEvents function


## -description

The <b>TdhEnumerateManifestProviderEvents</b> function retrieves the list of events present in the provider manifest.

## -parameters

### -param ProviderGuid [in]

A GUID that identifies the manifest provider whose list of events you want to retrieve.

### -param Buffer [out]

A user-allocated buffer to receive the list of events. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-provider_event_info">PROVIDER_EVENT_INFO</a>  structure.

### -param BufferSize [in, out]

The size, in bytes, of the buffer pointed to by the <i>ProviderInfo</i> parameter. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns <b>ERROR_INSUFFICIENT_BUFFER</b> and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

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
The size of the <i>ProviderInfo</i> buffer is too small. Use the required buffer size set in the <i>BufferSize</i> parameter to allocate a new buffer.

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
<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/tdh/ns-tdh-provider_event_info">PROVIDER_EVENT_INFO</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetmanifesteventinformation">TdhGetManifestEventInformation</a>