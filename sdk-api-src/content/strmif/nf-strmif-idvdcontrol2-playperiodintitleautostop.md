---
UID: NF:strmif.IDvdControl2.PlayPeriodInTitleAutoStop
title: IDvdControl2::PlayPeriodInTitleAutoStop (strmif.h)
description: The PlayPeriodInTitleAutoStop method starts playback in the specified title from the specified start time until the specified end time.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayPeriodInTitleAutoStop method","IDvdControl2.PlayPeriodInTitleAutoStop","IDvdControl2::PlayPeriodInTitleAutoStop","IDvdControl2PlayPeriodInTitleAutoStop","PlayPeriodInTitleAutoStop","PlayPeriodInTitleAutoStop method [DirectShow]","PlayPeriodInTitleAutoStop method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playperiodintitleautostop","strmif/IDvdControl2::PlayPeriodInTitleAutoStop"]
old-location: dshow\idvdcontrol2_playperiodintitleautostop.htm
tech.root: dshow
ms.assetid: 6c0d647c-a0c3-428e-8368-9204049dfea8
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],PlayPeriodInTitleAutoStop method, IDvdControl2.PlayPeriodInTitleAutoStop, IDvdControl2::PlayPeriodInTitleAutoStop, IDvdControl2PlayPeriodInTitleAutoStop, PlayPeriodInTitleAutoStop, PlayPeriodInTitleAutoStop method [DirectShow], PlayPeriodInTitleAutoStop method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playperiodintitleautostop, strmif/IDvdControl2::PlayPeriodInTitleAutoStop
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl2::PlayPeriodInTitleAutoStop
 - strmif/IDvdControl2::PlayPeriodInTitleAutoStop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.PlayPeriodInTitleAutoStop
---

# IDvdControl2::PlayPeriodInTitleAutoStop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PlayPeriodInTitleAutoStop</code> method starts playback in the specified title from the specified start time until the specified end time.

## -parameters

### -param ulTitle [in]

Value that specifies the title; this value must be from 1 through 99.

### -param pStartTime [in]

Pointer to a [DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) structure that specifies the time at which to start playing.

### -param pEndTime [in]

Pointer to a [DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) structure that specifies the time at which to stop playing.

### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.

### -param ppCmd [out]

Receives a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.

## -returns

Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

The actual start and end times are the times before or equal to the frame number specified in the <b>DVD_HMSF_TIMECODE</b>. The frame rate code is ignored on <i>pStartTime</i> and <i>pEndTime</i>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_TitleDVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>