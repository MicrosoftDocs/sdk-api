---
UID: NF:strmif.IMediaSeeking.SetPositions
title: IMediaSeeking::SetPositions (strmif.h)
description: The SetPositions method sets the current position and the stop position.
helpviewer_keywords: ["IMediaSeeking interface [DirectShow]","SetPositions method","IMediaSeeking.SetPositions","IMediaSeeking::SetPositions","IMediaSeekingSetPositions","SetPositions","SetPositions method [DirectShow]","SetPositions method [DirectShow]","IMediaSeeking interface","dshow.imediaseeking_setpositions","strmif/IMediaSeeking::SetPositions"]
old-location: dshow\imediaseeking_setpositions.htm
tech.root: dshow
ms.assetid: aa1369fd-a57a-4246-bb23-969f6ce3cad8
ms.date: 4/26/2023
ms.keywords: IMediaSeeking interface [DirectShow],SetPositions method, IMediaSeeking.SetPositions, IMediaSeeking::SetPositions, IMediaSeekingSetPositions, SetPositions, SetPositions method [DirectShow], SetPositions method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_setpositions, strmif/IMediaSeeking::SetPositions
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMediaSeeking::SetPositions
 - strmif/IMediaSeeking::SetPositions
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
 - IMediaSeeking.SetPositions
---

# IMediaSeeking::SetPositions


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetPositions</code> method sets the current position and the stop position.

## -parameters

### -param pCurrent [in, out]

[in,out] Pointer to a variable that specifies the current position, in units of the current time format.

### -param dwCurrentFlags [in]

Bitwise combination of flags. See Remarks.

### -param pStop [in, out]

[in,out] Pointer to a variable that specifies the stop time, in units of the current time format.

### -param dwStopFlags [in]

Bitwise combination of flags. See Remarks.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No position change. (Both flags specify no seeking.)

</td>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

The <i>dwCurrentFlags</i> and <i>dwStopFlags</i> parameters define the type of seek. The following flags are defined.

<table>
<tr>
<th>Positioning Flags
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>AM_SEEKING_NoPositioning</td>
<td>No change in position. (The time parameter can be <b>NULL</b>.)</td>
</tr>
<tr>
<td>AM_SEEKING_AbsolutePositioning</td>
<td>The specified position is absolute.</td>
</tr>
<tr>
<td>AM_SEEKING_RelativePositioning</td>
<td>The specified position is relative to the previous value.</td>
</tr>
<tr>
<td>AM_SEEKING_IncrementalPositioning</td>
<td>The stop position (<i>pStop</i>) is relative to the current position (<i>pCurrent</i>).</td>
</tr>
</table>
 

<table>
<tr>
<th>Modifier Flags
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>AM_SEEKING_SeekToKeyFrame</td>
<td>Seek to the nearest key frame. This might be faster, but less accurate. None of the filters that ship with DirectShow support this flag. Decoders are the most likely type of filter to support it.</td>
</tr>
<tr>
<td>AM_SEEKING_ReturnTime</td>
<td>Return the equivalent reference times.</td>
</tr>
<tr>
<td>AM_SEEKING_Segment</td>
<td>Use segment seeking.</td>
</tr>
<tr>
<td>AM_SEEKING_NoFlush</td>
<td>Do not flush.</td>
</tr>
</table>
 

For each parameter, use one positioning flag. Optionally, include one or more modifier flags.

If the AM_SEEKING_ReturnTime flag is specified, the method converts the position value to a reference time and returns it in the <i>pCurrent</i> or <i>pStop</i> variable. This flag is useful if you are using another time format, such as frames.

The AM_SEEKING_Segment and AM_SEEKING_NoFlush flags support seamless looping:

<ul>
<li>If the AM_SEEKING_Segment flag is present, the source filter sends an <a href="/windows/desktop/DirectShow/ec-end-of-segment">EC_END_OF_SEGMENT</a> event when it reaches the stop position, instead of calling <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endofstream">IPin::EndOfStream</a>. The application can wait for this event and then issue another seek command.</li>
<li>If the AM_SEEKING_NoFlush flag is present, the graph does not flush data during the seek. Use this flag with AM_SEEKING_Segment.</li>
</ul>
To perform looping, the graph must report AM_SEEKING_CanDoSegments in the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcapabilities">IMediaSeeking::GetCapabilities</a> method. Currently, only the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser Filter</a> supports this feature.

The incoming values of <i>pCurrent</i> and <i>pStop</i> are expressed in the current time format. The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method. If the AM_SEEKING_ReturnTime flag is present, the method converts the outgoing value to <b>REFERENCE_TIME</b> units.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
If you implement this method, you can check whether the caller is requesting a change in the current or stop position, by using the value AM_SEEKING_PositioningBitsMask to mask out the modifier flags. For example:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD dwCurrentPos = dwCurrentFlags &amp; AM_SEEKING_PositioningBitsMask
if (dwCurrentPos == AM_SEEKING_AbsolutePositioning)
{ 
    // Set new position to pCurrent.
    m_rtStart = *pCurrent;
}
else if (dwCurrentPos == AM_SEEKING_RelativePositioning)
{
    // Increment current position by pCurrent.
    m_rtStart += *pCurrent;
}
</pre>
</td>
</tr>
</table></span></div>
For more information, see the source code for the <a href="/windows/desktop/DirectShow/csourceseeking-setpositions">CSourceSeeking::SetPositions</a> method in the base class library.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>