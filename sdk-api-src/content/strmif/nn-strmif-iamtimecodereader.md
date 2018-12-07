---
UID: NN:strmif.IAMTimecodeReader
title: IAMTimecodeReader
author: windows-sdk-content
description: The IAMTimecodeReader interface reads SMPTE or MIDI timecode from an external device. The MSDV and MSTape drivers support this interface for reading timecode from an external DV or MPEG-2 camcorder.
old-location: dshow\iamtimecodereader.htm
tech.root: DirectShow
ms.assetid: 76c3f603-8abc-450a-adb2-f2a90cb1634d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMTimecodeReader, IAMTimecodeReader interface [DirectShow], IAMTimecodeReader interface [DirectShow],described, IAMTimecodeReaderInterface, dshow.iamtimecodereader, strmif/IAMTimecodeReader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTimecodeReader interface


## -description



The <b>IAMTimecodeReader</b> interface reads SMPTE or MIDI timecode from an external device. The <a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> and <a href="https://msdn.microsoft.com/aa59f322-09b1-4b0a-be6f-d865c20f76e5">MSTape</a> drivers support this interface for reading timecode from an external DV or MPEG-2 camcorder.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMTimecodeReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTimecodeReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04eda79a-1301-4bc1-855e-1cb0c4451797">get_VITCLine</a>
</td>
<td align="left" width="63%">
Retrieves the vertical interval line that the timecode reader is using to read timecode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227c5d8e-fbaf-4bf8-a8c8-954e14e51a24">GetTCRMode</a>
</td>
<td align="left" width="63%">
Retrieves properties of the timecode reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4ed646f-677e-4703-8197-036636f20561">GetTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the most recent timecode, userbits, and flag values available in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/171b0fd2-1498-41ae-9803-99b9128ee305">put_VITCLine</a>
</td>
<td align="left" width="63%">
Specifies the vertical interval line that the timecode reader will use to read timecode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd9f5310-b1c0-46ff-b038-d6a50ac400a2">SetTCRMode</a>
</td>
<td align="left" width="63%">
Sets the timecode reader properties.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the PROPSETID_TIMECODE_READER property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.

SMPTE timecode is a frame addressing system that identifies video and audio sources, makes automatic track synchronization possible, and provides a container for additional data related to the source material. SMPTE timecode's main purpose is to provide a machine-readable address for video and audio. It is displayed in hh:mm:ss:ff (hours, minutes, seconds, frames) format and is thoroughly defined in ANSI/SMPTE 12-1986.

Applications generally save timecode in one of two ways. It is either written to the capture file as an additional stream or as a discontinuity table stored in the extended AVI file index. It is commonly used to trigger capture or playback and to create edit decision lists that describes how source material is organized into a finished product.

If you intend to capture timecode, treat it as a separate stream that has its own media type. It can be consumed by an appropriate file-writing multiplexer filter. However, sometimes there are errors in reading the timecode off the tape because of dropouts and other mechanical tape problems. In such cases, the timecode source filter should simply drop samples and mark the next valid one with the discontinuity property.

If you intend to use timecodes to trigger capture or playback from a timecoded (or "striped") videotape, the sequence of events goes as follows:

<ol>
<li>Build a capture graph, open a target AVI file, and preallocate disk space if necessary. If the captured material will be appended to an existing AVI file, seek to the end of the file before writing. The capture graph is paused at this point.</li>
<li>Search the VCR to the capture start point and note the timecode. You can either enter this value manually into your program, or the application can automatically read it. Automatic reading requires that the graph is running but the stream control interfaces on the file multiplexer's input pins are discarding incoming samples, effectively gating the capture.</li>
<li>Cue the VCR to preroll position, usually five seconds before the target point.</li>
<li>Start the VCR and the graph. When the trigger point is reached (or the trigger point minus the file writer's preroll), the stream control interfaces release the file multiplexer and it begins streaming media samples to the file writer.</li>
<li>You can stop the capture process manually or by setting a duration property on the stream control interface.</li>
</ol>
You must consider discontinuous timecode, both during preroll and during the capture process; it is reasonable to demand that the timecode be continuous and monotonically increasing throughout the preroll and capture start point. This prevents a potentially ambiguous calculation of relative stream times by the <a href="https://msdn.microsoft.com/868ec03e-d4e5-4a1e-914a-6be8933f1c7c">IMediaSeeking::ConvertTimeFormat</a> method. Also, the timecode need not be the only gating signal for triggered capture. Any time-stamped data stored in the vertical blanking interval, such as Intercast or closed-captioned data (XDS), can be used to start the streaming of video and audio data to disk.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
See the <a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport</a> interface for hardware requirements.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
Implement this interface on an external device filter when you want to specify how an external device should read SMPTE/MIDI timecode information. Expose the <a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking</a> interface on your filter so that applications can convert timecode to reference time, using the <a href="https://msdn.microsoft.com/868ec03e-d4e5-4a1e-914a-6be8933f1c7c">IMediaSeeking::ConvertTimeFormat</a> method.

The external device must be able to read timecode and send it to the computer over its control interface. If this is not the case, you must either have a timecode reader card in your computer, or you can write a software decoder that converts VITC (Vertical Interval Timecode) in captured video frames or LTC (Linear Timecode) captured as an audio signal into DirectShow timecode samples.




## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

