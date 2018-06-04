---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFMediaSink::GetCharacteristics


## -description



Gets the characteristics of the media sink.




## -parameters




### -param pdwCharacteristics [out]


            Receives a bitwise <b>OR</b> of zero or more flags. The following flags are defined:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_FIXED_STREAMS"></a><a id="mediasink_fixed_streams"></a><dl>
<dt><b><b>MEDIASINK_FIXED_STREAMS</b></b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">

                The media sink has a fixed number of streams. It does not support the <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a> and <a href="https://msdn.microsoft.com/f99ee960-7fea-4867-bc24-d7e1d6fcafa5">IMFMediaSink::RemoveStreamSink</a> methods. This flag is a hint to the application.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CANNOT_MATCH_CLOCK"></a><a id="mediasink_cannot_match_clock"></a><dl>
<dt><b><b>MEDIASINK_CANNOT_MATCH_CLOCK</b></b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The media sink cannot match rates with an external clock.

For best results, this media sink should be used as the time source for the presentation clock. If any other time source is used, the media sink cannot match rates with the clock, with poor results (for example, glitching).

This flag should be used sparingly, because it limits how the pipeline can be configured.

For more information about the presentation clock, see <a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_RATELESS"></a><a id="mediasink_rateless"></a><dl>
<dt><b><b>MEDIASINK_RATELESS</b></b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The media sink is rateless. It consumes samples as quickly as possible, and does not synchronize itself to a presentation clock.

Most archiving sinks are rateless.

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CLOCK_REQUIRED"></a><a id="mediasink_clock_required"></a><dl>
<dt><b><b>MEDIASINK_CLOCK_REQUIRED</b></b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The media sink requires a presentation clock. The presentation clock is set by calling the media sink's <a href="https://msdn.microsoft.com/844fc3b3-b56e-4048-b589-e24457bcc419">IMFMediaSink::SetPresentationClock</a> method.

This flag is obsolete, because all media sinks must support the <a href="https://msdn.microsoft.com/844fc3b3-b56e-4048-b589-e24457bcc419">SetPresentationClock</a> method, even if the media sink ignores the clock (as in a rateless media sink).

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_CAN_PREROLL"></a><a id="mediasink_can_preroll"></a><dl>
<dt><b><b>MEDIASINK_CAN_PREROLL</b></b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">

                The media sink can accept preroll samples before the presentation clock starts. The media sink exposes the <a href="https://msdn.microsoft.com/7cc93751-4477-4649-b09e-53f519fb1acb">IMFMediaSinkPreroll</a> interface.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE"></a><a id="mediasink_require_reference_mediatype"></a><dl>
<dt><b><b>MEDIASINK_REQUIRE_REFERENCE_MEDIATYPE</b></b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The first stream sink (index 0) is a reference stream. The reference stream must have a media type before the media types can be set on the other stream sinks.

</td>
</tr>
</table>
 


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">

                The media sink's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.
              

</td>
</tr>
</table>
 




## -remarks




        The characteristics of a media sink are fixed throughout the life time of the sink.
      




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

