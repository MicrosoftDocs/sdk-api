---
UID: NN:sbe.IStreamBufferMediaSeeking
title: IStreamBufferMediaSeeking
author: windows-sdk-content
description: The IStreamBufferMediaSeeking interface controls seeking in a stream buffer source graph. The Stream Buffer Source filter exposes this interface.
old-location: mstv\istreambuffermediaseeking.htm
tech.root: mstv
ms.assetid: baac4c50-7aba-4bdc-93ad-57f22c55ea4b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamBufferMediaSeeking, IStreamBufferMediaSeeking interface [Microsoft TV Technologies], IStreamBufferMediaSeeking interface [Microsoft TV Technologies],described, IStreamBufferMediaSeekingInterface, mstv.istreambuffermediaseeking, sbe/IStreamBufferMediaSeeking
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferMediaSeeking
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferMediaSeeking interface


## -description


The <b>IStreamBufferMediaSeeking</b> interface controls seeking in a stream buffer source graph. The <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter exposes this interface.

The methods in this interface have exactly the same names and parameters as those in the <a href="https://msdn.microsoft.com/en-us/library/Dd407023(v=VS.85).aspx">IMediaSeeking</a> interface. To seek within a stream buffer file, use this interface directly on the source filter instead of calling <b>IMediaSeeking</b> methods on the filter graph.


## -remarks



When the Stream Buffer Source plays a recording created by the <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> object or the <a href="https://msdn.microsoft.com/4f7fcdee-f6e2-4288-a11c-f0076858be67">RecComp</a> object, it can seek anywhere within the file. When it plays a live stream from the Stream Buffer Sink, it can seek anywhere within the sink filter's buffer. This might include recorded content or temporary backing files. Transitions across files are seamless.

Live content from the Stream Buffer Sink grows on one end, as new content is recorded, and shrinks on the other end, as stale backing files are deleted. Therefore, the positioning information for this interface differs somewhat from the regular <a href="https://msdn.microsoft.com/en-us/library/Dd407023(v=VS.85).aspx">IMediaSeeking</a> interface. The following definitions are used.

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>Content start</td>
<td>
The time of the earliest available content. For live content, the value starts at zero and increases whenever the Stream Buffer Engine deletes an old file.

For example, if there are six backing files, each 15 minutes long, then after 60 minutes the content start jumps to 15 minutes, as the first file is deleted.

</td>
</tr>
<tr>
<td>Content stop</td>
<td>The time of the latest available content. For live content, this value starts at zero and increases continuously.</td>
</tr>
<tr>
<td>Segment stop</td>
<td>
The time when the Stream Buffer Source filter will stop playback. This value starts at positive infinity, but it can be set to arbitrary times by the application.

The segment stop time can be later than the content stop time, so it may not be possible to seek to this position. If playback reaches the end of the content before reaching the segment stop time, the graph sends an end-of-stream (EOS) event.

</td>
</tr>
<tr>
<td>Stream position</td>
<td>
The current playback position, relative to the content start.

For example, if the source graph runs for 15 seconds and pauses for 10 seconds, the stream position remains at 15 seconds until the source graph runs again.

</td>
</tr>
</table>
 

Given these definition, the following <b>IStreamBufferMediaSeeking</b> methods have special behaviors:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407026(v=VS.85).aspx">GetAvailable</a>: Returns content start and content stop.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407028(v=VS.85).aspx">GetCurrentPosition</a>: Returns stream position.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407029(v=VS.85).aspx">GetDuration</a>: Returns (content start –content stop).</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407030(v=VS.85).aspx">GetPositions</a>: Returns stream position and segment stop.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407033(v=VS.85).aspx">GetStopPosition</a>: Returns segment stop.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd407038(v=VS.85).aspx">SetPositions</a>: Sets stream position and segment stop.</li>
</ul>
The only time format supported by this interface is reference time (TIME_FORMAT_MEDIA_TIME). The Stream Buffer Engine does not support frame-accurate seeking.

<h3><a id="Rate_Changes"></a><a id="rate_changes"></a><a id="RATE_CHANGES"></a>Rate Changes</h3>
For rate changes, the playback speed must be greater than 0.1 or less than -0.1. Negative rates indicate reverse playback. If the capture source is an MPEG-2 source, the <a href="https://msdn.microsoft.com/fc3ed646-2644-4dc3-b84b-a00fef95df66">MPEG-2 Video Analyzer</a> filter is required to support playback faster than 4x or reverse playback. For more information, see <a href="https://msdn.microsoft.com/1883182f-0a07-4a66-acb7-1c64955471e2">Creating Stream Buffer Graphs</a>.

The <b>IStreamBufferMediaSeeking::SetRate</b> method may return VFW_E_DVD_WRONG_SPEED if the requested rate is too high for very short content. This error is caused when the Stream Buffer Engine cannot get I frames for the available content at the requested rate.

The <b>SetRate</b> method may also return E_NOTIMPL. This error code can happen if several decoders are registered on the user's system. If so, use the standard <a href="https://msdn.microsoft.com/en-us/library/Dd407039(v=VS.85).aspx">IMediaSeeking::SetRate</a> method on the source graph to set the playback rate. The <a href="https://msdn.microsoft.com/en-us/library/Dd407023(v=VS.85).aspx">IMediaSeeking</a> version of <b>SetRate</b> may return VFW_E_UNSUPPORTED_AUDIO, which indicates that the audio decoder does not support trick mode. It is safe to ignore this error code.

The <b>IStreamBufferMediaSeeking</b> version of <b>SetRate</b> may also fail if the decoder does not support rates other than 1x speed.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferMediaSeeking)</code>.




## -see-also




<a href="https://msdn.microsoft.com/cc0490ac-bc0d-472c-b0a7-5e0f81054921">Buffering in the Stream Buffer Engine</a>



<a href="https://msdn.microsoft.com/fc3ed646-2644-4dc3-b84b-a00fef95df66">MPEG-2 Video Analyzer Filter</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

