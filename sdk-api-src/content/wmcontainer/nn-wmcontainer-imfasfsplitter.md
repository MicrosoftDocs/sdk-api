---
UID: NN:wmcontainer.IMFASFSplitter
title: IMFASFSplitter (wmcontainer.h)
author: windows-sdk-content
description: Provides methods to read data from an Advanced Systems Format (ASF) file.
old-location: mf\imfasfsplitter.htm
tech.root: medfound
ms.assetid: 75d8b2a3-7c50-4dd5-8927-b11eb9f12602
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 75d8b2a3-7c50-4dd5-8927-b11eb9f12602, IMFASFSplitter, IMFASFSplitter interface [Media Foundation], IMFASFSplitter interface [Media Foundation],described, mf.imfasfsplitter, wmcontainer/IMFASFSplitter
ms.topic: interface
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFSplitter interface


## -description


Provides methods to read data from an Advanced Systems Format (ASF) file. The ASF splitter object exposes this interface. To create the ASF splitter, <a href="https://msdn.microsoft.com/05936a66-ed39-4645-adfb-5816b9981771">MFCreateASFSplitter</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFSplitter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFSplitter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFSplitter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be92c734-2bcb-4a7c-bd62-fb545c3c7762">Flush</a>
</td>
<td align="left" width="63%">
Resets the ASF splitter and releases all pending samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba008e4a-98ad-4633-8b80-1d2ffce04b9c">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the option flags that are set on the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59a6c53c-2cdf-4677-a5a3-4138f107f721">GetLastSendTime</a>
</td>
<td align="left" width="63%">
Retrieves the send time of the last sample received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85133059-6710-4fb2-b42b-f54747816f9c">GetNextSample</a>
</td>
<td align="left" width="63%">
Retrieves a sample from the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2c12e45-f320-43e0-abf1-36993dfed32d">GetSelectedStreams</a>
</td>
<td align="left" width="63%">
Retrieves a list of currently selected streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd69c2f9-dabf-4bba-bb3b-75ec3208c189">Initialize</a>
</td>
<td align="left" width="63%">
Resets the ASF splitter and configures it to receive ASF data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13457c17-ab35-47a3-8e83-00eef7686841">ParseData</a>
</td>
<td align="left" width="63%">
Sends packetized ASF data to the ASF splitter for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a241f8a4-7609-4a6c-825f-a7b882bfc25f">SelectStreams</a>
</td>
<td align="left" width="63%">
Sets the streams to be parsed by the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c70e5a0-7dd5-49c5-af35-4d9568871b41">SetFlags</a>
</td>
<td align="left" width="63%">
Sets option flags on the ASF splitter.

</td>
</tr>
</table> 


## -remarks



The ASF splitter accepts ASF packets and extracts the samples for individual streams from them. As with the other ASF base components, the ASF splitter object must be initialized with data from an ASF ContentInfo object before use.




## -see-also




<a href="https://msdn.microsoft.com/383b1cc6-4a77-4e0e-a766-6213c64b025c">ASF Splitter</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

