---
UID: NF:icodecapi.ICodecAPI.RegisterForEvent
title: ICodecAPI::RegisterForEvent
ms.date: 09/22/2020
targetos: Windows
description: The RegisterForEvent method registers the application to receive events from the codec. (ICodecAPI::RegisterForEvent)
helpviewer_keywords: ["A proprietary event GUID defined by the codec.","CODECAPI_CHANGELISTS","ICodecAPI interface [DirectShow]","RegisterForEvent method","ICodecAPI.RegisterForEvent","ICodecAPI::RegisterForEvent","ICodecAPIRegisterForEvent","One of the property GUIDs defined in codecapi.h. (See Codec API Properties.)","RegisterForEvent","RegisterForEvent method [DirectShow]","RegisterForEvent method [DirectShow]","ICodecAPI interface","dshow.icodecapi_registerforevent","icodecapi/ICodecAPI::RegisterForEvent"]
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icodecapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - icodecapi.h
api_name:
 - ICodecAPI::RegisterForEvent
f1_keywords:
 - ICodecAPI::RegisterForEvent
 - icodecapi/ICodecAPI::RegisterForEvent
dev_langs:
 - c++
---

## -description

The <b>RegisterForEvent</b> method registers the application to receive events from the codec.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the event.
There are three categories of events:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CODECAPI_CHANGELISTS"></a><a id="codecapi_changelists"></a><dl>
<dt><b>CODECAPI_CHANGELISTS</b></dt>
</dl>
</td>
<td width="60%">
The codec notifies the application when the properties of the codec change.  The event data is a list of GUIDs for the properties that changed.

</td>
</tr>
<tr>
<td width="40%"><a id="One_of_the_property_GUIDs_defined_in_codecapi.h.__See_Codec_API_Properties._"></a><a id="one_of_the_property_guids_defined_in_codecapi.h.__see_codec_api_properties._"></a><a id="ONE_OF_THE_PROPERTY_GUIDS_DEFINED_IN_CODECAPI.H.__SEE_CODEC_API_PROPERTIES._"></a><dl>
<dt><b>One of the property GUIDs defined in codecapi.h. (See <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.)</b></dt>
</dl>
</td>
<td width="60%">
The codec notifies the application when the specified  property changes.  Typically, a codec will support this type of notification for a limited set of properties, if any.

</td>
</tr>
<tr>
<td width="40%"><a id="A_proprietary_event_GUID_defined_by_the_codec."></a><a id="a_proprietary_event_guid_defined_by_the_codec."></a><a id="A_PROPRIETARY_EVENT_GUID_DEFINED_BY_THE_CODEC."></a><dl>
<dt><b>A proprietary event GUID defined by the codec.</b></dt>
</dl>
</td>
<td width="60%">
Implementation dependent.

</td>
</tr>
</table>


### -param userData [out]

Pointer to caller-defined data. The application receives this pointer in the <i>lParam1</i> event parameter.

## -returns

This method can return one of these values.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. The codec does not support event notification, or does not support the event GUID specified in the <i>Api</i> parameter.

</td>
</tr>
</table>

## -remarks

The application receives an <a href="/windows/desktop/DirectShow/ec-codecapi-event">EC_CODECAPI_EVENT</a> event notification whenever the encoder codec sends the event.  To get the event, uses the <a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface.

The <i>lParam2</i> parameter of the event is a pointer to a <a href="/windows/desktop/api/strmif/ns-strmif-codecapieventdata">CodecAPIEventData</a> structure. This structure can be followed by additional data, depending on the event GUID. The size of this  data is given by the <b>dataLength</b> member.

<table>
<tr>
<th>GUID</th>
<th>Event Data</th>
</tr>
<tr>
<td>CODECAPI_CHANGELISTS</td>
<td>An array of GUIDs. Each GUID specifies a codec property whose current value or valid range has changed. The size of the array is <b>dataLength</b> / <code>sizeof(GUID)</code>.</td>
</tr>
<tr>
<td>A property GUID defined in codecapi.h. </td>
<td>None.</td>
</tr>
<tr>
<td>Proprietary event GUID.</td>
<td>Implementation dependent.</td>
</tr>
</table>
 

If the codec does not support the specified event, the method returns <b>E_NOTIMPL</b>. The codec might support other events.

To disable notifications for an event, call <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-unregisterforevent">ICodecAPI::UnregisterForEvent</a>.

## -see-also


<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>

