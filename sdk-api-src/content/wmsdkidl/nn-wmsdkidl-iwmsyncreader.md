---
UID: NN:wmsdkidl.IWMSyncReader
title: IWMSyncReader (wmsdkidl.h)
description: The IWMSyncReader interface provides the ability to read ASF files using synchronous calls.
old-location: wmformat\iwmsyncreader.htm
tech.root: wmformat
ms.assetid: 2a46e79f-084e-4173-ad0f-211d3065d81a
ms.date: 12/05/2018
ms.keywords: IWMSyncReader, IWMSyncReader interface [windows Media Format], IWMSyncReader interface [windows Media Format],described, IWMSyncReaderInterface, wmformat.iwmsyncreader, wmsdkidl/IWMSyncReader
f1_keywords:
- wmsdkidl/IWMSyncReader
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSyncReader interface


## -description



The <b>IWMSyncReader</b> interface provides the ability to read ASF files using synchronous calls. This is in contrast to many of the methods in <b>IWMReader</b>, which are called asynchronously.

You get a pointer to an <b>IWMSyncReader</b> interface when you create a new synchronous reader object with a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatesyncreader">WMCreateSyncReader</a>.

In addition to enabling synchronous reading, the methods of <b>IWMSyncReader</b> are tailored to meet the demands of editing applications. Default playback from <b>IWMSyncReader</b> delivers uncompressed samples for the default streams of all outputs. However, you can manipulate the selected streams during streaming without having to enable manual stream selection. You can also receive compressed or uncompressed samples, though you cannot change between them during streaming. Samples are delivered by either output number or stream number, so you can receive uncompressed samples from mutually exclusive streams.

Many of the methods in this interface are almost identical to corresponding methods in the asynchronous reader.

Use of this interface, as well as the implementation of an <b>IStream</b> COM object that passes data to this object, is demonstrated in the WMSyncReader SDK sample.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSyncReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSyncReader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-close">Close</a>
</td>
<td align="left" width="63%">
Removes a file from the synchronous reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample">GetNextSample</a>
</td>
<td align="left" width="63%">
Gets the next sample from the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of outputs in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves one output format for one output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of formats supported by an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream">GetOutputNumberForStream</a>
</td>
<td align="left" width="63%">
Retrieves the output number that corresponds to a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples">GetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether a stream is configured to deliver uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput">GetStreamNumberForOutput</a>
</td>
<td align="left" width="63%">
Retrieves the current stream number that corresponds to an output number in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamselected">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Retrieves whether or not a particular stream is selected for sample delivery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-open">Open</a>
</td>
<td align="left" width="63%">
Opens a file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops">SetOutputProps</a>
</td>
<td align="left" width="63%">
Sets the properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Sets a named setting for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange">SetRange</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe">SetRangeByFrame</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback based upon the frame number of a frame-indexed video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples">SetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Sets a stream to deliver compressed or uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setstreamsselected">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Sets the streams for which the reader will deliver samples.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by calling the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

