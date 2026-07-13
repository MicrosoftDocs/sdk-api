---
UID: NF:mfidl.IMFMediaSink.GetCharacteristics
title: IMFMediaSink::GetCharacteristics (mfidl.h)
description: Gets the characteristics of the media sink.
helpviewer_keywords: ["GetCharacteristics","GetCharacteristics method [Media Foundation]","GetCharacteristics method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","GetCharacteristics method","IMFMediaSink.GetCharacteristics","IMFMediaSink::GetCharacteristics","MEDIASINK_CANNOT_MATCH_CLOCK","MEDIASINK_CAN_PREROLL","MEDIASINK_CLOCK_REQUIRED","MEDIASINK_FIXED_STREAMS","MEDIASINK_RATELESS","MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE","a7e8e2af-8b10-47f5-8b09-a7147ace5ba1","mf.imfmediasink_getcharacteristics","mfidl/IMFMediaSink::GetCharacteristics"]
old-location: mf\imfmediasink_getcharacteristics.htm
tech.root: mf
ms.assetid: a7e8e2af-8b10-47f5-8b09-a7147ace5ba1
ms.date: 12/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Media Foundation], GetCharacteristics method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetCharacteristics method, IMFMediaSink.GetCharacteristics, IMFMediaSink::GetCharacteristics, MEDIASINK_CANNOT_MATCH_CLOCK, MEDIASINK_CAN_PREROLL, MEDIASINK_CLOCK_REQUIRED, MEDIASINK_FIXED_STREAMS, MEDIASINK_RATELESS, MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE, a7e8e2af-8b10-47f5-8b09-a7147ace5ba1, mf.imfmediasink_getcharacteristics, mfidl/IMFMediaSink::GetCharacteristics
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
 - IMFMediaSink::GetCharacteristics
 - mfidl/IMFMediaSink::GetCharacteristics
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
 - IMFMediaSink.GetCharacteristics
---

# IMFMediaSink::GetCharacteristics


## -description

Gets the characteristics of the media sink.

## -parameters

### -param pdwCharacteristics [out]

Receives a bitwise <b>OR</b> of zero or more flags. The following flags are defined:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_FIXED_STREAMS"></a><a id="mediasink_fixed_streams"></a><dl>
<dt><b>MEDIASINK_FIXED_STREAMS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The media sink has a fixed number of streams. It does not support the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink">IMFMediaSink::RemoveStreamSink</a> methods. This flag is a hint to the application.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CANNOT_MATCH_CLOCK"></a><a id="mediasink_cannot_match_clock"></a><dl>
<dt><b>MEDIASINK_CANNOT_MATCH_CLOCK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The media sink cannot match rates with an external clock.

For best results, this media sink should be used as the time source for the presentation clock. If any other time source is used, the media sink cannot match rates with the clock, with poor results (for example, glitching).

This flag should be used sparingly, because it limits how the pipeline can be configured.

For more information about the presentation clock, see <a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_RATELESS"></a><a id="mediasink_rateless"></a><dl>
<dt><b>MEDIASINK_RATELESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The media sink is rateless. It consumes samples as quickly as possible, and does not synchronize itself to a presentation clock.

Most archiving sinks are rateless.

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CLOCK_REQUIRED"></a><a id="mediasink_clock_required"></a><dl>
<dt><b>MEDIASINK_CLOCK_REQUIRED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The media sink requires a presentation clock. The presentation clock is set by calling the media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock">IMFMediaSink::SetPresentationClock</a> method.

This flag is obsolete, because all media sinks must support the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock">SetPresentationClock</a> method, even if the media sink ignores the clock (as in a rateless media sink).

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CAN_PREROLL"></a><a id="mediasink_can_preroll"></a><dl>
<dt><b>MEDIASINK_CAN_PREROLL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The media sink can accept preroll samples before the presentation clock starts. The media sink exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll">IMFMediaSinkPreroll</a> interface.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE"></a><a id="mediasink_require_reference_mediatype"></a><dl>
<dt><b>MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The first stream sink (index 0) is a reference stream. The reference stream must have a media type before the media types can be set on the other stream sinks.

</td>
</tr>
</table>

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
</table>

## -remarks

The characteristics of a media sink are fixed throughout the life time of the sink.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>