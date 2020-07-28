---
UID: NF:strmif.ICodecAPI.RegisterForEvent
title: ICodecAPI::RegisterForEvent (strmif.h)
description: The RegisterForEvent method registers the application to receive events from the codec.
helpviewer_keywords: ["A proprietary event GUID defined by the codec.","CODECAPI_CHANGELISTS","ICodecAPI interface [DirectShow]","RegisterForEvent method","ICodecAPI.RegisterForEvent","ICodecAPI::RegisterForEvent","ICodecAPIRegisterForEvent","One of the property GUIDs defined in codecapi.h. (See Codec API Properties.)","RegisterForEvent","RegisterForEvent method [DirectShow]","RegisterForEvent method [DirectShow]","ICodecAPI interface","dshow.icodecapi_registerforevent","strmif/ICodecAPI::RegisterForEvent"]
old-location: dshow\icodecapi_registerforevent.htm
tech.root: dshow
ms.assetid: 87423ddb-7011-40ab-a449-eb43688efb26
ms.date: 12/05/2018
ms.keywords: A proprietary event GUID defined by the codec., CODECAPI_CHANGELISTS, ICodecAPI interface [DirectShow],RegisterForEvent method, ICodecAPI.RegisterForEvent, ICodecAPI::RegisterForEvent, ICodecAPIRegisterForEvent, One of the property GUIDs defined in codecapi.h. (See Codec API Properties.), RegisterForEvent, RegisterForEvent method [DirectShow], RegisterForEvent method [DirectShow],ICodecAPI interface, dshow.icodecapi_registerforevent, strmif/ICodecAPI::RegisterForEvent
f1_keywords:
- strmif/ICodecAPI.RegisterForEvent
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- ICodecAPI.RegisterForEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI::RegisterForEvent


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
<dt><b>One of the property GUIDs defined in codecapi.h. (See <a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.)</b></dt>
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



The application receives an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-codecapi-event">EC_CODECAPI_EVENT</a> event notification whenever the encoder codec sends the event.  To get the event, uses the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface.

The <i>lParam2</i> parameter of the event is a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-codecapieventdata">CodecAPIEventData</a> structure. This structure can be followed by additional data, depending on the event GUID. The size of this  data is given by the <b>dataLength</b> member.

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

To disable notifications for an event, call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-unregisterforevent">ICodecAPI::UnregisterForEvent</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
 

 

