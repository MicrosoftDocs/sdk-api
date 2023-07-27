---
UID: NF:strmif.IAMTimecodeReader.GetTimecode
title: IAMTimecodeReader::GetTimecode (strmif.h)
description: The GetTimecode method retrieves the most recent timecode, userbit, and flag values available in the stream.
helpviewer_keywords: ["GetTimecode","GetTimecode method [DirectShow]","GetTimecode method [DirectShow]","IAMTimecodeReader interface","IAMTimecodeReader interface [DirectShow]","GetTimecode method","IAMTimecodeReader.GetTimecode","IAMTimecodeReader::GetTimecode","IAMTimecodeReaderGetTimecode","dshow.iamtimecodereader_gettimecode","strmif/IAMTimecodeReader::GetTimecode"]
old-location: dshow\iamtimecodereader_gettimecode.htm
tech.root: dshow
ms.assetid: c4ed646f-677e-4703-8197-036636f20561
ms.date: 4/26/2023
ms.keywords: GetTimecode, GetTimecode method [DirectShow], GetTimecode method [DirectShow],IAMTimecodeReader interface, IAMTimecodeReader interface [DirectShow],GetTimecode method, IAMTimecodeReader.GetTimecode, IAMTimecodeReader::GetTimecode, IAMTimecodeReaderGetTimecode, dshow.iamtimecodereader_gettimecode, strmif/IAMTimecodeReader::GetTimecode
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
 - IAMTimecodeReader::GetTimecode
 - strmif/IAMTimecodeReader::GetTimecode
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
 - IAMTimecodeReader.GetTimecode
---

# IAMTimecodeReader::GetTimecode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetTimecode</code> method retrieves the most recent timecode, userbit, and flag values available in the stream.

## -parameters

### -param pTimecodeSample [out]

Pointer to a <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Use this method to monitor the timecode and to parse duplicates and discontinuities.

The timecode contains undefined bits, called <i>userbits</i>. Applications can use these bits to store synchronization information or other custom information.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>
The <a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> driver supports reading SMPTE timecode or absolute track numbers (ATN). The <a href="/windows/desktop/DirectShow/mstape-driver">MSTape</a> driver supports reading the relative time counter (RTC). To read time information on these devices, do the following:

Set the <b>dwFlags</b> member of the <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure to one of the following values.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_DEVCAP_TIMECODE_READ</td>
<td>Timecode (DV)</td>
</tr>
<tr>
<td>ED_DEVCAP_ATN_READ</td>
<td>Absolute track number (DV)</td>
</tr>
<tr>
<td>ED_DEVCAP_RTC_READ</td>
<td>Relative time counter (MPEG tape)</td>
</tr>
</table>
 

The <b>timecode</b> member of the <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure is a <a href="/windows/desktop/DirectShow/getting-timecode-from-the-device">TIMECODE</a> structure. Initialize that structure's <b>dwFrames</b> member to zero.

All other structure members are ignored.

When the method returns, the <b>dwFrames</b> member contains the time information, in the following format.

<table>
<tr>
<th>Time Information</th>
<th>Format</th>
</tr>
<tr>
<td>Timecode</td>
<td>Hours, minutes, seconds, and frames, as a binary coded decimal (BCD) value: <i>0xhhmmssff</i>.</td>
</tr>
<tr>
<td>ATN</td>
<td>Track number.</td>
</tr>
<tr>
<td>RTC</td>
<td>Hours, minutes, seconds, and frames, as a BCD value: <i>0xhhmmssff</i>. The most significant bit of the frames byte is a sign bit. If the frame count is not available, the remaining frame bits are set to 0x7F.</td>
</tr>
</table>
 

Also, the <b>dwUser</b> member receives the <i>blank flag</i> bit from the device, which has one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0x00</td>
<td>Not a discontinuity.</td>
</tr>
<tr>
<td>0x01</td>
<td>Discontinuity. </td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/getting-timecode-from-the-device">Getting Timecode from the Device</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>