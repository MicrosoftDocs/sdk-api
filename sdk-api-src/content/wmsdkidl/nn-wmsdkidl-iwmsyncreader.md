---
UID: NN:wmsdkidl.IWMSyncReader
title: IWMSyncReader (wmsdkidl.h)
author: windows-sdk-content
description: The IWMSyncReader interface provides the ability to read ASF files using synchronous calls.
old-location: wmformat\iwmsyncreader.htm
tech.root: wmformat
ms.assetid: 2a46e79f-084e-4173-ad0f-211d3065d81a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSyncReader, IWMSyncReader interface [windows Media Format], IWMSyncReader interface [windows Media Format],described, IWMSyncReaderInterface, wmformat.iwmsyncreader, wmsdkidl/IWMSyncReader
ms.topic: interface
req.header: wmsdkidl.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMSyncReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader interface


## -description



The <b>IWMSyncReader</b> interface provides the ability to read ASF files using synchronous calls. This is in contrast to many of the methods in <b>IWMReader</b>, which are called asynchronously.

You get a pointer to an <b>IWMSyncReader</b> interface when you create a new synchronous reader object with a call to <a href="https://msdn.microsoft.com/en-us/library/Dd757788(v=VS.85).aspx">WMCreateSyncReader</a>.

In addition to enabling synchronous reading, the methods of <b>IWMSyncReader</b> are tailored to meet the demands of editing applications. Default playback from <b>IWMSyncReader</b> delivers uncompressed samples for the default streams of all outputs. However, you can manipulate the selected streams during streaming without having to enable manual stream selection. You can also receive compressed or uncompressed samples, though you cannot change between them during streaming. Samples are delivered by either output number or stream number, so you can receive uncompressed samples from mutually exclusive streams.

Many of the methods in this interface are almost identical to corresponding methods in the asynchronous reader.

Use of this interface, as well as the implementation of an <b>IStream</b> COM object that passes data to this object, is demonstrated in the WMSyncReader SDK sample.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSyncReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMSyncReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSyncReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798584(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Removes a file from the synchronous reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798585(v=VS.85).aspx">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798586(v=VS.85).aspx">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798587(v=VS.85).aspx">GetNextSample</a>
</td>
<td align="left" width="63%">
Gets the next sample from the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798588(v=VS.85).aspx">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of outputs in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798589(v=VS.85).aspx">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves one output format for one output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798590(v=VS.85).aspx">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of formats supported by an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798591(v=VS.85).aspx">GetOutputNumberForStream</a>
</td>
<td align="left" width="63%">
Retrieves the output number that corresponds to a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798592(v=VS.85).aspx">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798593(v=VS.85).aspx">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798594(v=VS.85).aspx">GetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether a stream is configured to deliver uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798595(v=VS.85).aspx">GetStreamNumberForOutput</a>
</td>
<td align="left" width="63%">
Retrieves the current stream number that corresponds to an output number in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798596(v=VS.85).aspx">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Retrieves whether or not a particular stream is selected for sample delivery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798597(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens a file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798598(v=VS.85).aspx">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798599(v=VS.85).aspx">SetOutputProps</a>
</td>
<td align="left" width="63%">
Sets the properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798600(v=VS.85).aspx">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Sets a named setting for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798704(v=VS.85).aspx">SetRange</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798705(v=VS.85).aspx">SetRangeByFrame</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback based upon the frame number of a frame-indexed video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798706(v=VS.85).aspx">SetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Sets a stream to deliver compressed or uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798707(v=VS.85).aspx">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Sets the streams for which the reader will deliver samples.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by calling the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

