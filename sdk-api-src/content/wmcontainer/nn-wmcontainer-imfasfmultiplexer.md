---
UID: NN:wmcontainer.IMFASFMultiplexer
title: IMFASFMultiplexer (wmcontainer.h)
description: Provides methods to create Advanced Systems Format (ASF) data packets.
helpviewer_keywords: ["IMFASFMultiplexer","IMFASFMultiplexer interface [Media Foundation]","IMFASFMultiplexer interface [Media Foundation]","described","bdb549b5-425b-4f77-b413-723ceb7acd11","mf.imfasfmultiplexer","wmcontainer/IMFASFMultiplexer"]
old-location: mf\imfasfmultiplexer.htm
tech.root: medfound
ms.assetid: bdb549b5-425b-4f77-b413-723ceb7acd11
ms.date: 12/05/2018
ms.keywords: IMFASFMultiplexer, IMFASFMultiplexer interface [Media Foundation], IMFASFMultiplexer interface [Media Foundation],described, bdb549b5-425b-4f77-b413-723ceb7acd11, mf.imfasfmultiplexer, wmcontainer/IMFASFMultiplexer
f1_keywords:
- wmcontainer/IMFASFMultiplexer
dev_langs:
- c++
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
- IMFASFMultiplexer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFMultiplexer interface


## -description


Provides methods to create Advanced Systems Format (ASF) data packets. The methods of this interface process input samples into the packets that make up an ASF data section. The ASF multiplexer exposes this interface. To create the ASF multiplexer, call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer">MFCreateASFMultiplexer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFMultiplexer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFMultiplexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFMultiplexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end">End</a>
</td>
<td align="left" width="63%">
Collects data from the multiplexer and updates the ASF ContentInfo object to include that information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush">Flush</a>
</td>
<td align="left" width="63%">
Signals the multiplexer to process all queued samples. Call this method after passing the last sample to the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags indicating the configured multiplexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket">GetNextPacket</a>
</td>
<td align="left" width="63%">
Retrieves the next output ASF packet from the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves multiplexer statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the multiplexer with the data from an ASF ContentInfo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample">ProcessSample</a>
</td>
<td align="left" width="63%">
Delivers input samples to the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets multiplexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setsynctolerance">SetSyncTolerance</a>
</td>
<td align="left" width="63%">
Sets the maximum time by which samples from various streams can be out of synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-multiplexer">ASF Multiplexer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

