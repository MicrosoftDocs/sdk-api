---
UID: NS:medparam._MP_ENVELOPE_SEGMENT
title: MP_ENVELOPE_SEGMENT (medparam.h)
description: The MP_ENVELOPE_SEGMENT structure defines an envelope segment used by an envelope-following parameter.
helpviewer_keywords: ["MPF_ENVLP_BEGIN_CURRENTVAL","MPF_ENVLP_BEGIN_NEUTRALVAL","MPF_ENVLP_STANDARD","MP_ENVELOPEStructure","MP_ENVELOPE_SEGMENT","MP_ENVELOPE_SEGMENT structure [DirectShow]","dshow.mp_envelope_segment","medparam/MP_ENVELOPE_SEGMENT"]
old-location: dshow\mp_envelope_segment.htm
tech.root: dshow
ms.assetid: b7386b63-c563-42dd-851c-780bf1043f65
ms.date: 4/26/2023
ms.keywords: MPF_ENVLP_BEGIN_CURRENTVAL, MPF_ENVLP_BEGIN_NEUTRALVAL, MPF_ENVLP_STANDARD, MP_ENVELOPEStructure, MP_ENVELOPE_SEGMENT, MP_ENVELOPE_SEGMENT structure [DirectShow], dshow.mp_envelope_segment, medparam/MP_ENVELOPE_SEGMENT
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MP_ENVELOPE_SEGMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MP_ENVELOPE_SEGMENT
 - medparam/_MP_ENVELOPE_SEGMENT
 - MP_ENVELOPE_SEGMENT
 - medparam/MP_ENVELOPE_SEGMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_ENVELOPE_SEGMENT
---

# MP_ENVELOPE_SEGMENT structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MP_ENVELOPE_SEGMENT</code> structure defines an envelope segment used by an envelope-following parameter.

## -struct-fields

### -field rtStart

Start time of the segment, relative to the time stamp on the first buffer, in 100-nanosecond units.

### -field rtEnd

Stop time of the segment, relative to the time stamp on the first buffer, in 100-nanosecond units.

### -field valStart

Initial value of the parameter, at the start of the segment.

### -field valEnd

Final value of the parameter, at the end of the segment.

### -field iCurve

Member of the <b>MP_CURVE_TYPE</b> enumerated type that specifies the curve followed by the parameter.

### -field flags

Specifies one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPF_ENVLP_STANDARD"></a><a id="mpf_envlp_standard"></a><dl>
<dt><b>MPF_ENVLP_STANDARD</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Use all the information provided with the envelope segment.

</td>
</tr>
<tr>
<td width="40%"><a id="MPF_ENVLP_BEGIN_CURRENTVAL"></a><a id="mpf_envlp_begin_currentval"></a><dl>
<dt><b>MPF_ENVLP_BEGIN_CURRENTVAL</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Ignore the specified start value. Start from the current value.

</td>
</tr>
<tr>
<td width="40%"><a id="MPF_ENVLP_BEGIN_NEUTRALVAL"></a><a id="mpf_envlp_begin_neutralval"></a><dl>
<dt><b>MPF_ENVLP_BEGIN_NEUTRALVAL</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Ignore the specified start value. Start from the neutral value. (See <a href="/previous-versions/windows/desktop/api/medparam/ns-medparam-mp_paraminfo">MP_PARAMINFO</a>.)

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>