---
UID: NF:mfidl.IMFMediaSession.Start
title: IMFMediaSession::Start (mfidl.h)
description: Starts the Media Session.
helpviewer_keywords: ["1bdec0c0-b042-4e5e-a72b-b15942750ced","GUID_NULL","IMFMediaSession interface [Media Foundation]","Start method","IMFMediaSession.Start","IMFMediaSession::Start","MF_TIME_FORMAT_ENTRY_RELATIVE","MF_TIME_FORMAT_SEGMENT_OFFSET","Start","Start method [Media Foundation]","Start method [Media Foundation]","IMFMediaSession interface","mf.imfmediasession_start","mfidl/IMFMediaSession::Start"]
old-location: mf\imfmediasession_start.htm
tech.root: mf
ms.assetid: 1bdec0c0-b042-4e5e-a72b-b15942750ced
ms.date: 12/05/2018
ms.keywords: 1bdec0c0-b042-4e5e-a72b-b15942750ced, GUID_NULL, IMFMediaSession interface [Media Foundation],Start method, IMFMediaSession.Start, IMFMediaSession::Start, MF_TIME_FORMAT_ENTRY_RELATIVE, MF_TIME_FORMAT_SEGMENT_OFFSET, Start, Start method [Media Foundation], Start method [Media Foundation],IMFMediaSession interface, mf.imfmediasession_start, mfidl/IMFMediaSession::Start
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSession::Start
 - mfidl/IMFMediaSession::Start
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
 - IMFMediaSession.Start
---

# IMFMediaSession::Start


## -description

Starts the Media Session.

## -parameters

### -param pguidTimeFormat [in]

Pointer to a GUID that specifies the time format for the <i>pvarStartPosition</i> parameter. This parameter can be <b>NULL</b>. The value <b>NULL</b> is equivalent to passing in <b>GUID_NULL</b>.

The following time format GUIDs are defined:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_NULL"></a><a id="guid_null"></a><dl>
<dt><b>GUID_NULL</b></dt>
</dl>
</td>
<td width="60%">
Presentation time. The <i>pvarStartPosition</i> parameter must have one of the following <b>PROPVARIANT</b> types.

<ul>
<li><b>VT_I8</b>: The <i>pvarStartPosition</i> parameter contains the starting position in 100-nanosecond units, relative to the start of the presentation.</li>
<li><b>VT_EMPTY</b>: Playback starts from the current position.</li>
</ul>
All media sources support this time format.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TIME_FORMAT_SEGMENT_OFFSET"></a><a id="mf_time_format_segment_offset"></a><dl>
<dt><b>MF_TIME_FORMAT_SEGMENT_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
Segment offset. This time format is supported by the <a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>. The starting time is an offset within a segment.

Call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset">MFCreateSequencerSegmentOffset</a> function to create the <b>PROPVARIANT</b> value for the 
<i>pvarStartPosition</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TIME_FORMAT_ENTRY_RELATIVE"></a><a id="mf_time_format_entry_relative"></a><dl>
<dt><b>MF_TIME_FORMAT_ENTRY_RELATIVE</b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>
Skip to a playlist entry. The <i>pvarStartPosition</i> parameter specifies the index of the playlist entry, relative to the current entry. For example, the value 2 skips forward two entries. To skip backward, pass a negative value. The <b>PROPVARIANT</b> type is <b>VT_I4</b>.

If a media source supports this time format, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics">IMFMediaSource::GetCharacteristics</a> method returns one or both of the following flags:

<ul>
<li><b>MFMEDIASOURCE_CAN_SKIPFORWARD</b></li>
<li><b>MFMEDIASOURCE_CAN_SKIPBACKWARD</b></li>
</ul>
</td>
</tr>
</table>

### -param pvarStartPosition [in]

Pointer to a <b>PROPVARIANT</b> that specifies the starting position for playback. The meaning and data type of this parameter are indicated by the <i>pguidTimeFormat</i> parameter.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed in the Media Session's current state.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.
              

</td>
</tr>
</table>

## -remarks

When this method is called, the Media Session starts the presentation clock and begins to process media samples.

This method is asynchronous. When the method completes, the Media Session sends an <a href="/windows/desktop/medfound/mesessionstarted">MESessionStarted</a> event.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>