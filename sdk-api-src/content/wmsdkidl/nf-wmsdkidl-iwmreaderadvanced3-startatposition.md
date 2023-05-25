---
UID: NF:wmsdkidl.IWMReaderAdvanced3.StartAtPosition
title: IWMReaderAdvanced3::StartAtPosition (wmsdkidl.h)
description: The StartAtPosition method enables you to specify a starting position for a file using one of several offset formats.
helpviewer_keywords: ["IWMReaderAdvanced3 interface [windows Media Format]","StartAtPosition method","IWMReaderAdvanced3.StartAtPosition","IWMReaderAdvanced3::StartAtPosition","IWMReaderAdvanced3StartAtPosition","StartAtPosition","StartAtPosition method [windows Media Format]","StartAtPosition method [windows Media Format]","IWMReaderAdvanced3 interface","wmformat.iwmreaderadvanced3_startatposition","wmsdkidl/IWMReaderAdvanced3::StartAtPosition"]
old-location: wmformat\iwmreaderadvanced3_startatposition.htm
tech.root: wmformat
ms.assetid: 64b922be-3a8f-4cbe-aa1d-aa3833e1f0fa
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced3 interface [windows Media Format],StartAtPosition method, IWMReaderAdvanced3.StartAtPosition, IWMReaderAdvanced3::StartAtPosition, IWMReaderAdvanced3StartAtPosition, StartAtPosition, StartAtPosition method [windows Media Format], StartAtPosition method [windows Media Format],IWMReaderAdvanced3 interface, wmformat.iwmreaderadvanced3_startatposition, wmsdkidl/IWMReaderAdvanced3::StartAtPosition
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderAdvanced3::StartAtPosition
 - wmsdkidl/IWMReaderAdvanced3::StartAtPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced3.StartAtPosition
---

# IWMReaderAdvanced3::StartAtPosition


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StartAtPosition</b> method enables you to specify a starting position for a file using one of several offset formats. This method is very similar to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a>, except that the starting position and duration can be given for time, video frame number, SMPTE time code, or playlist position. If you only need to seek on presentation time, use <b>Start</b>.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which <i>pvOffsetStart</i> and <i>pvDuration</i> apply. Passing zero signifies that the offset start and duration apply for all streams in the file. If you pass zero, the only valid values for <i>dwOffsetFormat</i> are WMT_OFFSET_FORMAT_100NS and WMT_OFFSET_FORMAT_PLAYLIST_OFFSET.

### -param pvOffsetStart [in]

Void pointer to the address containing the offset start. The unit of measurement for the offset is determined by <i>dwOffsetFormat</i>. The unit of measurement also dictates the size of the variable pointed to. The possible variable types are listed according to offset format in the following table.

<table>
<tr>
<th>Offset format
                </th>
<th><i>pvOffsetStart</i> data type
                </th>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_100NS</td>
<td><b>QWORD</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_FRAME_NUMBERS</td>
<td><b>QWORD</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_PLAYLIST_OFFSET</td>
<td><b>LONG</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_TIMECODE</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data">WMT_TIMECODE_EXTENSION_DATA</a>
</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_APPROXIMATE</td>
<td><b>QWORD</b></td>
</tr>
</table>

### -param pvDuration [in]

Void pointer to the address containing the duration of playback. If zero is passed, playback will continue until the end of the file. The unit of measurement for the duration is determined by <i>dwOffsetFormat</i>. The unit of measurement also dictates the size of the variable pointed to. The possible variable types are listed according to offset format in the following table.

<table>
<tr>
<th>Offset format
                </th>
<th><i>pvDuration</i> data type
                </th>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_100NS</td>
<td><b>QWORD</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_FRAME_NUMBERS</td>
<td><b>QWORD</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_PLAYLIST_OFFSET</td>
<td><b>QWORD</b></td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_TIMECODE</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data">WMT_TIMECODE_EXTENSION_DATA</a>
</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_APPROXIMATE</td>
<td><b>QWORD</b></td>
</tr>
</table>

### -param dwOffsetFormat [in]

<b>DWORD</b> containing one member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format">WMT_OFFSET_FORMAT</a> enumeration type. Valid values and their meanings are as follows.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_100NS</td>
<td>The offset and duration are specified in 100-nanosecond units. This is the same offset format that is supported by the <b>IWMReader::Start</b> method.</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_FRAME_NUMBERS</td>
<td>The offset is specified by the video frame number at which to start playback. The duration is a number of video frames.</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_PLAYLIST_OFFSET</td>
<td>The offset is specified by an offset into a playlist. The duration is specified in 100-nanosecond units.</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_TIMECODE</td>
<td>The offset is specified by a SMPTE time code value. The duration is not a count, but another SMPTE time code value.</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_APPROXIMATE</td>
<td>The offset and duration are specified in 100-nanosecond units. When this format is used, playback begins with the closest clean point prior to the time provided. This format is intended to decrease seeking time when the exact sample is not required, such as in a player application's seek bar.</td>
</tr>
</table>

### -param fRate [in]

Floating point number indicating playback rate. Normal-speed playback is 1.0; higher numbers cause faster playback, and lower numbers cause slower playback. Numbers less than zero indicate reverse rate (rewinding). The valid range is 1.0 through 10.0, and -1.0 through -10.0.

### -param pvContext [in]

Generic pointer, for use by the application. This pointer is passed back to the application on calls to <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback</a>.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>dwOffsetFormat</i> is WMT_OFFSET_FORMAT_FRAME_NUMBERS and <i>wStreamNum</i> is zero.

OR

<i>pvOffsetStart</i> is <b>NULL</b>, signifying a resume, and the reader is in stop mode. You cannot resume playback when the player has been stopped.

OR

<i>pvOffsetStart</i> is <b>NULL</b>, signifying a resume, and <i>pvDuration</i> is not <b>NULL</b>. You cannot specify a duration for a resume.

OR

No file is open in the reader.

OR

<i>fRate</i> is out of bounds.

OR

The reader receiving broadcast streams. You cannot seek from a broadcasting source.

OR

<i>fRate</i> is negative, indicating a rewind, and the duration would rewind to before the beginning of the file.

OR

<i>dwOffsetFormat</i> is WMT_OFFSET_FORMAT_FRAME_NUMBERS and the file is not indexed and/or is not indexed by frame.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for a message structure required internally.

</td>
</tr>
</table>

## -remarks

Frame-based access is available only for local files. You cannot use <b>StartAtPosition</b> to specify starting frame numbers for streamed content, even if the file is indexed by frame.

You can pass <b>NULL</b> for <i>pvOffsetStart</i> if you are making a call to resume paused playback. In this case you must also pass <b>NULL</b> for <i>pvDuration</i>.

If an invalid duration is specified, <b>StartAtPosition</b> will not fail. As many samples as possible will be delivered.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>