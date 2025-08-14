---
UID: NF:winevt.EvtGetEventMetadataProperty
title: EvtGetEventMetadataProperty function (winevt.h)
description: Gets the specified event metadata property.
helpviewer_keywords: ["EvtGetEventMetadataProperty","EvtGetEventMetadataProperty function [EventLog]","wes.evtgeteventmetadataproperty","winevt/EvtGetEventMetadataProperty"]
old-location: wes\evtgeteventmetadataproperty.htm
tech.root: wes
ms.assetid: 2a5c53e3-bbb4-4245-a640-86b58d1a3c52
ms.date: 12/05/2018
ms.keywords: EvtGetEventMetadataProperty, EvtGetEventMetadataProperty function [EventLog], wes.evtgeteventmetadataproperty, winevt/EvtGetEventMetadataProperty
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
 - EvtGetEventMetadataProperty
 - winevt/EvtGetEventMetadataProperty
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
 - EvtGetEventMetadataProperty
---

# EvtGetEventMetadataProperty function


## -description

Gets the specified event metadata property.

## -parameters

### -param EventMetadata [in]

A handle to the event metadata that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtnexteventmetadata">EvtNextEventMetadata</a> function returns.

### -param PropertyId [in]

The identifier of the metadata property to retrieve. For a list of property identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_event_metadata_property_id">EVT_EVENT_METADATA_PROPERTY_ID</a> enumeration.

### -param Flags [in]

Reserved. Must be zero.

### -param EventMetadataPropertyBufferSize [in]

The size of the <i>EventMetadataPropertyBuffer</i> buffer, in bytes.

### -param EventMetadataPropertyBuffer [in]

A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param EventMetadataPropertyBufferUsed [out]

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

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtnexteventmetadata">EvtNextEventMetadata</a>