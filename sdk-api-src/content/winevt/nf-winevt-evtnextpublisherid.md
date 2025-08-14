---
UID: NF:winevt.EvtNextPublisherId
title: EvtNextPublisherId function (winevt.h)
description: Gets the identifier of a provider from the enumerator.
helpviewer_keywords: ["EvtNextPublisherId","EvtNextPublisherId function [EventLog]","wes.evtnextpublisherid","winevt/EvtNextPublisherId"]
old-location: wes\evtnextpublisherid.htm
tech.root: wes
ms.assetid: e6cea6de-79f3-416b-9501-8d86f2579aa8
ms.date: 12/05/2018
ms.keywords: EvtNextPublisherId, EvtNextPublisherId function [EventLog], wes.evtnextpublisherid, winevt/EvtNextPublisherId
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtNextPublisherId
 - winevt/EvtNextPublisherId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
api_name:
 - EvtNextPublisherId
---

# EvtNextPublisherId function


## -description

Gets the identifier of a provider from the enumerator.

## -parameters

### -param PublisherEnum [in]

A handle to the registered providers enumerator that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublisherenum">EvtOpenPublisherEnum</a> function returns.

### -param PublisherIdBufferSize [in]

The size of the <i>PublisherIdBuffer</i> buffer, in characters.

### -param PublisherIdBuffer [in]

A caller-allocated buffer that will receive the name of the registered provider. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param PublisherIdBufferUsed [out]

The size, in characters, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

Call this function in a loop until the function returns <b>FALSE</b> and the error code is ERROR_NO_MORE_ITEMS.

This list of provider names is not sorted alphabetically.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublishermetadata">EvtOpenPublisherMetadata</a>