---
UID: NS:strmif.tagTIMECODE_SAMPLE
title: TIMECODE_SAMPLE (strmif.h)
description: The TIMECODE_SAMPLE structure contains complete timecode information.
helpviewer_keywords: ["*PTIMECODE_SAMPLE","AM_TIMECODE_COLORFRAME","AM_TIMECODE_COLORSEQUENCE","AM_TIMECODE_FILMSEQUENCE_TYPE","AM_TIMECODE_FLAG_CF","AM_TIMECODE_FLAG_DF","AM_TIMECODE_FLAG_FCM","AM_TIMECODE_FLAG_FIELD","ED_DEVCAP_ATN_READ","ED_DEVCAP_RTC_READ","ED_DEVCAP_TIMECODE_READ","TIMECODE_SAMPLE","TIMECODE_SAMPLE structure [DirectShow]","TIMECODE_SAMPLEStructure","dshow.timecode_sample","strmif/TIMECODE_SAMPLE","tagTIMECODE_SAMPLE"]
old-location: dshow\timecode_sample.htm
tech.root: dshow
ms.assetid: 7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be
ms.date: 4/26/2023
ms.keywords: '*PTIMECODE_SAMPLE, AM_TIMECODE_COLORFRAME, AM_TIMECODE_COLORSEQUENCE, AM_TIMECODE_FILMSEQUENCE_TYPE, AM_TIMECODE_FLAG_CF, AM_TIMECODE_FLAG_DF, AM_TIMECODE_FLAG_FCM, AM_TIMECODE_FLAG_FIELD, ED_DEVCAP_ATN_READ, ED_DEVCAP_RTC_READ, ED_DEVCAP_TIMECODE_READ, TIMECODE_SAMPLE, TIMECODE_SAMPLE structure [DirectShow], TIMECODE_SAMPLEStructure, dshow.timecode_sample, strmif/TIMECODE_SAMPLE, tagTIMECODE_SAMPLE'
req.header: strmif.h
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
req.typenames: TIMECODE_SAMPLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTIMECODE_SAMPLE
 - strmif/tagTIMECODE_SAMPLE
 - TIMECODE_SAMPLE
 - strmif/TIMECODE_SAMPLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - TIMECODE_SAMPLE
---

# TIMECODE_SAMPLE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>TIMECODE_SAMPLE</code> structure contains complete timecode information.

## -struct-fields

### -field qwTick

Reference time, in 100-nanosecond units.

### -field timecode

<a href="/windows/desktop/DirectShow/getting-timecode-from-the-device">TIMECODE</a> structure.

### -field dwUser

Packed SMPTE userbits.

### -field dwFlags

Timecode flag masks. Specify one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_FCM"></a><a id="am_timecode_flag_fcm"></a><dl>
<dt><b>AM_TIMECODE_FLAG_FCM</b></dt>
</dl>
</td>
<td width="60%">
Frame code mode; 0 = nondrop; 1 = drop.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_CF"></a><a id="am_timecode_flag_cf"></a><dl>
<dt><b>AM_TIMECODE_FLAG_CF</b></dt>
</dl>
</td>
<td width="60%">
Color frame flag.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_FIELD"></a><a id="am_timecode_flag_field"></a><dl>
<dt><b>AM_TIMECODE_FLAG_FIELD</b></dt>
</dl>
</td>
<td width="60%">
Field flag.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FLAG_DF"></a><a id="am_timecode_flag_df"></a><dl>
<dt><b>AM_TIMECODE_FLAG_DF</b></dt>
</dl>
</td>
<td width="60%">
Drop frame flag (from flags in actual timecode on external media).

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_COLORFRAME"></a><a id="am_timecode_colorframe"></a><dl>
<dt><b>AM_TIMECODE_COLORFRAME</b></dt>
</dl>
</td>
<td width="60%">
Specifies frame in color sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_COLORSEQUENCE"></a><a id="am_timecode_colorsequence"></a><dl>
<dt><b>AM_TIMECODE_COLORSEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
Duration in frames of complete sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="AM_TIMECODE_FILMSEQUENCE_TYPE"></a><a id="am_timecode_filmsequence_type"></a><dl>
<dt><b>AM_TIMECODE_FILMSEQUENCE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
One of the FILM_SEQUENCE_XXX defines.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_TIMECODE_READ"></a><a id="ed_devcap_timecode_read"></a><dl>
<dt><b>ED_DEVCAP_TIMECODE_READ</b></dt>
</dl>
</td>
<td width="60%">
Read SMPTE timecode; applies to DV camcorders.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_ATN_READ"></a><a id="ed_devcap_atn_read"></a><dl>
<dt><b>ED_DEVCAP_ATN_READ</b></dt>
</dl>
</td>
<td width="60%">
Read the absolute track number (ATN); applies to DV camcorders. This constant is defined in the header file Xprtdefs.h.

</td>
</tr>
<tr>
<td width="40%"><a id="ED_DEVCAP_RTC_READ"></a><a id="ed_devcap_rtc_read"></a><dl>
<dt><b>ED_DEVCAP_RTC_READ</b></dt>
</dl>
</td>
<td width="60%">
Read the relative time counter (RTC); applies to MPEG camcorders. This constant is defined in the header file Xprtdefs.h.

</td>
</tr>
</table>

## -remarks

The upper 16 bits in <b>dwFlags</b> are reserved; set to zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-gettimecode">IAMTimecodeReader::GetTimecode</a>