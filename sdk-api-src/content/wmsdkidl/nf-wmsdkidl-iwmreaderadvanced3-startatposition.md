---
UID: NF:wmsdkidl.IWMReaderAdvanced3.StartAtPosition
title: IWMReaderAdvanced3::StartAtPosition
author: windows-driver-content
description: The StartAtPosition method enables you to specify a starting position for a file using one of several offset formats.
old-location: wmformat\iwmreaderadvanced3_startatposition.htm
old-project: wmformat
ms.assetid: 64b922be-3a8f-4cbe-aa1d-aa3833e1f0fa
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMReaderAdvanced3 interface [windows Media Format],StartAtPosition method, IWMReaderAdvanced3.StartAtPosition, IWMReaderAdvanced3::StartAtPosition, IWMReaderAdvanced3StartAtPosition, StartAtPosition, StartAtPosition method [windows Media Format], StartAtPosition method [windows Media Format],IWMReaderAdvanced3 interface, wmformat.iwmreaderadvanced3_startatposition, wmsdkidl/IWMReaderAdvanced3::StartAtPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced3.StartAtPosition
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced3::StartAtPosition


## -description



The <b>StartAtPosition</b> method enables you to specify a starting position for a file using one of several offset formats. This method is very similar to <a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a>, except that the starting position and duration can be given for time, video frame number, SMPTE time code, or playlist position. If you only need to seek on presentation time, use <b>Start</b>.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which <i>pvOffsetStart</i> and <i>pvDuration</i> apply. Passing zero signifies that the offset start and duration apply for all streams in the file. If you pass zero, the only valid values for <i>dwOffsetFormat</i> are WMT_OFFSET_FORMAT_100NS and WMT_OFFSET_FORMAT_PLAYLIST_OFFSET.


### -param pvOffsetStart [in]

Void pointer to the address containing the offset start. The unit of measurement for the offset is determined by <i>dwOffsetFormat</i>. The unit of measurement also dictates the size of the variable pointed to. The possible variable types are listed according to offset format in the following table.

<table>
<tr>
<th>
                  Offset format
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
<a href="https://msdn.microsoft.com/039c352c-d1f0-443f-acef-f730e949725c">WMT_TIMECODE_EXTENSION_DATA</a>
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
<th>
                  Offset format
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
<a href="https://msdn.microsoft.com/039c352c-d1f0-443f-acef-f730e949725c">WMT_TIMECODE_EXTENSION_DATA</a>
</td>
</tr>
<tr>
<td>WMT_OFFSET_FORMAT_APPROXIMATE</td>
<td><b>QWORD</b></td>
</tr>
</table>
 


### -param dwOffsetFormat [in]

<b>DWORD</b> containing one member of the <a href="https://msdn.microsoft.com/b4119098-0407-462b-8550-46f8c1312fe0">WMT_OFFSET_FORMAT</a> enumeration type. Valid values and their meanings are as follows.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
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

Generic pointer, for use by the application. This pointer is passed back to the application on calls to <a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback</a>.


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




<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>
 

 

