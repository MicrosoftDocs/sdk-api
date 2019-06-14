---
UID: NN:mfidl.IMFSequencerSource
title: IMFSequencerSource (mfidl.h)
author: windows-sdk-content
description: Implemented by the Sequencer Source.
old-location: mf\imfsequencersource.htm
tech.root: medfound
ms.assetid: ba5e8e7b-5b0e-4807-a459-75bd5727d1e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSequencerSource, IMFSequencerSource interface [Media Foundation], IMFSequencerSource interface [Media Foundation],described, ba5e8e7b-5b0e-4807-a459-75bd5727d1e2, mf.imfsequencersource, mfidl/IMFSequencerSource
ms.topic: interface
req.header: mfidl.h
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
 - IMFSequencerSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSequencerSource interface


## -description


Implemented by the <a href="https://docs.microsoft.com/windows/desktop/medfound/sequencer-source">Sequencer Source</a>. The sequencer source enables an application to create a sequence of topologies. To create the sequencer source, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource">MFCreateSequencerSource</a>. For step-by-step instructions about how to create a playlist, see <a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-create-a-playlist">How to Create a Playlist</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSequencerSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSequencerSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSequencerSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology">AppendTopology</a>
</td>
<td align="left" width="63%">
Adds a topology to the end of the queue of topologies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology">DeleteTopology</a>
</td>
<td align="left" width="63%">
Deletes a topology from the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-getpresentationcontext">GetPresentationContext</a>
</td>
<td align="left" width="63%">
Maps a presentation descriptor to its associated sequencer element identifier and topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology">UpdateTopology</a>
</td>
<td align="left" width="63%">
Updates a topology in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags">UpdateTopologyFlags</a>
</td>
<td align="left" width="63%">
Updates the flags for a topology in the queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sequencer-source">Sequencer Source</a>
 

 

