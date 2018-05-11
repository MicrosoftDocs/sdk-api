---
UID: NN:wmsdkidl.IWMSyncReader
title: IWMSyncReader
author: windows-driver-content
description: The IWMSyncReader interface provides the ability to read ASF files using synchronous calls.
old-location: wmformat\iwmsyncreader.htm
old-project: wmformat
ms.assetid: 2a46e79f-084e-4173-ad0f-211d3065d81a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMSyncReader, IWMSyncReader interface [windows Media Format], IWMSyncReader interface [windows Media Format],described, IWMSyncReaderInterface, wmformat.iwmsyncreader, wmsdkidl/IWMSyncReader
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMSyncReader
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader interface


## -description



The <b>IWMSyncReader</b> interface provides the ability to read ASF files using synchronous calls. This is in contrast to many of the methods in <b>IWMReader</b>, which are called asynchronously.

You get a pointer to an <b>IWMSyncReader</b> interface when you create a new synchronous reader object with a call to <a href="https://msdn.microsoft.com/77cb65cc-9785-4af4-9b92-245c17e5ab82">WMCreateSyncReader</a>.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Removes a file from the synchronous reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84fbc2c7-001b-4339-a7df-89914274a72b">GetMaxOutputSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b098985-4eb2-4292-a9b9-cfdd051e9c0e">GetMaxStreamSampleSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum sample size for a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948047b3-3b87-4381-9320-c9602716ade2">GetNextSample</a>
</td>
<td align="left" width="63%">
Gets the next sample from the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fde0a136-6c13-43d9-9969-e1226be60f76">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of outputs in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7faac9e7-ad5f-42a4-ba6e-562ae973f81b">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves one output format for one output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f66784-791b-4f1b-8ba2-300a4521ce03">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of formats supported by an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/605f5a66-aa06-4d4e-998e-1a3f7d1c7be6">GetOutputNumberForStream</a>
</td>
<td align="left" width="63%">
Retrieves the output number that corresponds to a stream in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e701ea-8b53-4abe-8b78-7c6fb151d80f">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b96c84fd-a2e0-4fdb-a9c1-2e42b73f7a3e">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb903723-fd4b-4b1c-aa2f-e3c9f74dcebd">GetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether a stream is configured to deliver uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85543b80-78dd-4dc6-8885-c6a53f910165">GetStreamNumberForOutput</a>
</td>
<td align="left" width="63%">
Retrieves the current stream number that corresponds to an output number in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcde749e-c0fd-4be8-8708-a053854a9275">GetStreamSelected</a>
</td>
<td align="left" width="63%">
Retrieves whether or not a particular stream is selected for sample delivery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef42495a-2565-4925-882e-c3c42f9d418b">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5575fd7c-5eb0-4e4a-957d-e3fc174316ff">SetOutputProps</a>
</td>
<td align="left" width="63%">
Sets the properties of an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8deb322f-8b52-46cf-9b5c-76fa34b6bde2">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Sets a named setting for an output in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d96c97ad-085d-4753-8efb-8a6bcb284e78">SetRange</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d53838c-0d07-4aa6-8797-9ed7e07cb8fe">SetRangeByFrame</a>
</td>
<td align="left" width="63%">
Sets a start time and duration for playback based upon the frame number of a frame-indexed video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf998ecc-e80e-4eb3-9cba-61bd0b665d51">SetReadStreamSamples</a>
</td>
<td align="left" width="63%">
Sets a stream to deliver compressed or uncompressed samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d62a61cb-3b5a-4ce8-9677-92e280449d26">SetStreamsSelected</a>
</td>
<td align="left" width="63%">
Sets the streams for which the reader will deliver samples.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by calling the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

