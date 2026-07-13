---
UID: NF:winevt.EvtGetPublisherMetadataProperty
title: EvtGetPublisherMetadataProperty function (winevt.h)
description: Gets the specified provider metadata property.
helpviewer_keywords: ["EvtGetPublisherMetadataProperty","EvtGetPublisherMetadataProperty function [EventLog]","wes.evtgetpublishermetadataproperty","winevt/EvtGetPublisherMetadataProperty"]
old-location: wes\evtgetpublishermetadataproperty.htm
tech.root: wes
ms.assetid: f85a46ef-873c-4dd9-8b5c-3763fd67fc06
ms.date: 12/05/2018
ms.keywords: EvtGetPublisherMetadataProperty, EvtGetPublisherMetadataProperty function [EventLog], wes.evtgetpublishermetadataproperty, winevt/EvtGetPublisherMetadataProperty
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
 - EvtGetPublisherMetadataProperty
 - winevt/EvtGetPublisherMetadataProperty
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
 - EvtGetPublisherMetadataProperty
---

# EvtGetPublisherMetadataProperty function


## -description

Gets the specified provider metadata property.

## -parameters

### -param PublisherMetadata [in]

A handle to the metadata that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublishermetadata">EvtOpenPublisherMetadata</a> function returns.

### -param PropertyId [in]

The identifier of the metadata property to retrieve. For a list of property identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_publisher_metadata_property_id">EVT_PUBLISHER_METADATA_PROPERTY_ID</a> enumeration.

### -param Flags [in]

Reserved. Must be zero.

### -param PublisherMetadataPropertyBufferSize [in]

The size of the <i>PublisherMetadataPropertyBuffer</i> buffer, in bytes.

### -param PublisherMetadataPropertyBuffer [in]

A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param PublisherMetadataPropertyBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

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

<div class="alert"><b>Caution</b>  <p class="note">
<a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventmetadataproperty">EvtGetEventMetadataProperty</a> can return many different kinds of values in the <i>EventMetadataPropertyBuffer</i> variable. If <i>EventMetadataPropertyBuffer</i>-&gt;Type == <b>EvtVarTypeEvtHandle</b> then <i>EventMetadataPropertyBuffer</i> contains a handle that needs to be freed. When you are done with the handle, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function. 

</div>
<div> </div>

#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublishermetadata">EvtOpenPublisherMetadata</a>