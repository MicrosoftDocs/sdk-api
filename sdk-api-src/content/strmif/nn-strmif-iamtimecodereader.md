---
UID: NN:strmif.IAMTimecodeReader
title: IAMTimecodeReader (strmif.h)
description: The IAMTimecodeReader interface reads SMPTE or MIDI timecode from an external device. The MSDV and MSTape drivers support this interface for reading timecode from an external DV or MPEG-2 camcorder.
helpviewer_keywords: ["IAMTimecodeReader","IAMTimecodeReader interface [DirectShow]","IAMTimecodeReader interface [DirectShow]","described","IAMTimecodeReaderInterface","dshow.iamtimecodereader","strmif/IAMTimecodeReader"]
old-location: dshow\iamtimecodereader.htm
tech.root: dshow
ms.assetid: 76c3f603-8abc-450a-adb2-f2a90cb1634d
ms.date: 12/05/2018
ms.keywords: IAMTimecodeReader, IAMTimecodeReader interface [DirectShow], IAMTimecodeReader interface [DirectShow],described, IAMTimecodeReaderInterface, dshow.iamtimecodereader, strmif/IAMTimecodeReader
f1_keywords:
- strmif/IAMTimecodeReader
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeReader interface


## -description



The <b>IAMTimecodeReader</b> interface reads SMPTE or MIDI timecode from an external device. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/msdv-driver">MSDV</a> and <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mstape-driver">MSTape</a> drivers support this interface for reading timecode from an external DV or MPEG-2 camcorder.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTimecodeReader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-get_vitcline">get_VITCLine</a>
</td>
<td align="left" width="63%">
Retrieves the vertical interval line that the timecode reader is using to read timecode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-gettcrmode">GetTCRMode</a>
</td>
<td align="left" width="63%">
Retrieves properties of the timecode reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-gettimecode">GetTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the most recent timecode, userbits, and flag values available in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-put_vitcline">put_VITCLine</a>
</td>
<td align="left" width="63%">
Specifies the vertical interval line that the timecode reader will use to read timecode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-settcrmode">SetTCRMode</a>
</td>
<td align="left" width="63%">
Sets the timecode reader properties.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the PROPSETID_TIMECODE_READER property set. For more information, see the <a href="https://msdn.microsoft.com/library/ff554690(VS.85).aspx">Windows Driver Kit (WDK)</a> documentation.

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
You must consider discontinuous timecode, both during preroll and during the capture process; it is reasonable to demand that the timecode be continuous and monotonically increasing throughout the preroll and capture start point. This prevents a potentially ambiguous calculation of relative stream times by the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-converttimeformat">IMediaSeeking::ConvertTimeFormat</a> method. Also, the timecode need not be the only gating signal for triggered capture. Any time-stamped data stored in the vertical blanking interval, such as Intercast or closed-captioned data (XDS), can be used to start the streaming of video and audio data to disk.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
See the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a> interface for hardware requirements.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
Implement this interface on an external device filter when you want to specify how an external device should read SMPTE/MIDI timecode information. Expose the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> interface on your filter so that applications can convert timecode to reference time, using the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-converttimeformat">IMediaSeeking::ConvertTimeFormat</a> method.

The external device must be able to read timecode and send it to the computer over its control interface. If this is not the case, you must either have a timecode reader card in your computer, or you can write a software decoder that converts VITC (Vertical Interval Timecode) in captured video frames or LTC (Linear Timecode) captured as an audio signal into DirectShow timecode samples.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

