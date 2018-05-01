---
UID: NF:strmif.ICodecAPI.RegisterForEvent
title: ICodecAPI::RegisterForEvent method
author: windows-driver-content
description: The RegisterForEvent method registers the application to receive events from the codec.
old-location: dshow\icodecapi_registerforevent.htm
old-project: DirectShow
ms.assetid: 87423ddb-7011-40ab-a449-eb43688efb26
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: A proprietary event GUID defined by the codec., CODECAPI_CHANGELISTS, ICodecAPI, ICodecAPI interface [DirectShow], RegisterForEvent method, ICodecAPI::RegisterForEvent, ICodecAPIRegisterForEvent, One of the property GUIDs defined in codecapi.h. (See Codec API Properties.), RegisterForEvent method [DirectShow], RegisterForEvent method [DirectShow], ICodecAPI interface, RegisterForEvent,ICodecAPI.RegisterForEvent, dshow.icodecapi_registerforevent, strmif/ICodecAPI::RegisterForEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICodecAPI.RegisterForEvent
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::RegisterForEvent method


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
<dt><b>One of the property GUIDs defined in codecapi.h. (See <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.)</b></dt>
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



The application receives an <a href="https://msdn.microsoft.com/88924ba9-707b-41a7-9bca-c630b4a9c4c8">EC_CODECAPI_EVENT</a> event notification whenever the encoder codec sends the event.  To get the event, uses the <a href="https://msdn.microsoft.com/9d367b0a-c7ec-49d4-a41e-045ac81d2c51">IMediaEventEx</a> interface.

The <i>lParam2</i> parameter of the event is a pointer to a <a href="https://msdn.microsoft.com/04d0177d-ec9d-4f23-abd1-a37c787c24b2">CodecAPIEventData</a> structure. This structure can be followed by additional data, depending on the event GUID. The size of this  data is given by the <b>dataLength</b> member.

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

To disable notifications for an event, call <a href="https://msdn.microsoft.com/d6f48379-664a-498f-8872-2272778588db">ICodecAPI::UnregisterForEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>
 

 

