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
f1_keywords: 
 - "wmcontainer/IMFASFSplitter"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFSplitter interface


## -description


Provides methods to read data from an Advanced Systems Format (ASF) file. The ASF splitter object exposes this interface. To create the ASF splitter, <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter">MFCreateASFSplitter</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFSplitter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFSplitter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush">Flush</a>
</td>
<td align="left" width="63%">
Resets the ASF splitter and releases all pending samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the option flags that are set on the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getlastsendtime">GetLastSendTime</a>
</td>
<td align="left" width="63%">
Retrieves the send time of the last sample received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample">GetNextSample</a>
</td>
<td align="left" width="63%">
Retrieves a sample from the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams">GetSelectedStreams</a>
</td>
<td align="left" width="63%">
Retrieves a list of currently selected streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Resets the ASF splitter and configures it to receive ASF data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata">ParseData</a>
</td>
<td align="left" width="63%">
Sends packetized ASF data to the ASF splitter for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams">SelectStreams</a>
</td>
<td align="left" width="63%">
Sets the streams to be parsed by the ASF splitter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets option flags on the ASF splitter.

</td>
</tr>
</table> 


## -remarks



The ASF splitter accepts ASF packets and extracts the samples for individual streams from them. As with the other ASF base components, the ASF splitter object must be initialized with data from an ASF ContentInfo object before use.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

