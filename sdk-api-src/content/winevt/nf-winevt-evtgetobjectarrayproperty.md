---
UID: NF:winevt.EvtGetObjectArrayProperty
title: EvtGetObjectArrayProperty function (winevt.h)
description: Gets a provider metadata property from the specified object in the array.
helpviewer_keywords: ["EvtGetObjectArrayProperty","EvtGetObjectArrayProperty function [EventLog]","wes.evtgetobjectarrayproperty","winevt/EvtGetObjectArrayProperty"]
old-location: wes\evtgetobjectarrayproperty.htm
tech.root: wes
ms.assetid: a522f0a8-6050-4082-acdf-e700ebfa7efc
ms.date: 12/05/2018
ms.keywords: EvtGetObjectArrayProperty, EvtGetObjectArrayProperty function [EventLog], wes.evtgetobjectarrayproperty, winevt/EvtGetObjectArrayProperty
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
 - EvtGetObjectArrayProperty
 - winevt/EvtGetObjectArrayProperty
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
 - EvtGetObjectArrayProperty
---

# EvtGetObjectArrayProperty function


## -description

Gets a provider metadata property from the specified object in the array.

## -parameters

### -param ObjectArray [in]

A handle to an array of objects that the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a> function returns.

### -param PropertyId [in]

The property identifier of the metadata property that you want to get from the  specified object. For possible values, see the Remarks section of <a href="/windows/desktop/api/winevt/ne-winevt-evt_publisher_metadata_property_id">EVT_PUBLISHER_METADATA_PROPERTY_ID</a>.

### -param ArrayIndex [in]

The zero-based index of the object in the array.

### -param Flags [in]

Reserved. Must be zero.

### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.

### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param PropertyValueBufferUsed [out]

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

When you call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a> function with the following IDs, the function returns a handle to an array of objects of that type:

<ul>
<li>EvtPublisherMetadataChannelReferences</li>
<li>EvtPublisherMetadataLevels</li>
<li>EvtPublisherMetadataTasks</li>
<li>EvtPublisherMetadataOpcodes</li>
<li>EvtPublisherMetadataKeywords</li>
</ul>
For example, if you pass <b>EvtPublisherMetadataKeywords</b> to <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a>, the function returns a handle to an array of keyword objects.

To determine the size of the array, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetobjectarraysize">EvtGetObjectArraySize</a> function.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/ne-winevt-evt_publisher_metadata_property_id">EVT_PUBLISHER_METADATA_PROPERTY_ID</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a>