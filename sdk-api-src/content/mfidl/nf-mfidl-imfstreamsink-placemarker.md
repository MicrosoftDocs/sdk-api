---
UID: NF:mfidl.IMFStreamSink.PlaceMarker
title: IMFStreamSink::PlaceMarker (mfidl.h)
description: Places a marker in the stream.
helpviewer_keywords: ["IMFStreamSink interface [Media Foundation]","PlaceMarker method","IMFStreamSink.PlaceMarker","IMFStreamSink::PlaceMarker","PlaceMarker","PlaceMarker method [Media Foundation]","PlaceMarker method [Media Foundation]","IMFStreamSink interface","bfa4fb12-59b2-4599-b8ff-dc38750a5a79","mf.imfstreamsink_placemarker","mfidl/IMFStreamSink::PlaceMarker"]
old-location: mf\imfstreamsink_placemarker.htm
tech.root: mf
ms.assetid: bfa4fb12-59b2-4599-b8ff-dc38750a5a79
ms.date: 12/05/2018
ms.keywords: IMFStreamSink interface [Media Foundation],PlaceMarker method, IMFStreamSink.PlaceMarker, IMFStreamSink::PlaceMarker, PlaceMarker, PlaceMarker method [Media Foundation], PlaceMarker method [Media Foundation],IMFStreamSink interface, bfa4fb12-59b2-4599-b8ff-dc38750a5a79, mf.imfstreamsink_placemarker, mfidl/IMFStreamSink::PlaceMarker
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFStreamSink::PlaceMarker
 - mfidl/IMFStreamSink::PlaceMarker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink.PlaceMarker
---

# IMFStreamSink::PlaceMarker


## -description

Places a marker in the stream.

## -parameters

### -param eMarkerType [in]

Specifies the marker type, as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type">MFSTREAMSINK_MARKER_TYPE</a> enumeration.

### -param pvarMarkerValue [in]

Optional pointer to a <b>PROPVARIANT</b> that contains additional information related to the marker. The meaning of this value depends on the marker type. This parameter can be <b>NULL</b>.

### -param pvarContextValue [in]

Optional pointer to a <b>PROPVARIANT</b> that is attached to the <a href="/windows/desktop/medfound/mestreamsinkmarker">MEStreamSinkMarker</a> event. Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue">IMFMediaEvent::GetValue</a> to get this value from the event. The caller can use this information for any purpose. This parameter can be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.
              

</td>
</tr>
</table>

## -remarks

This method causes the stream sink to send an <a href="/windows/desktop/medfound/mestreamsinkmarker">MEStreamSinkMarker</a> event after the stream sink consumes all of the samples that were delivered up to this point (before the call to <b>PlaceMarker</b>).

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>