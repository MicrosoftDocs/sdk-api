---
UID: NF:mfidl.IMFSequencerSource.AppendTopology
title: IMFSequencerSource::AppendTopology (mfidl.h)
description: Adds a topology to the end of the queue.
helpviewer_keywords: ["4ff20d56-6095-495d-89ee-9086c61da8ac","AppendTopology","AppendTopology method [Media Foundation]","AppendTopology method [Media Foundation]","IMFSequencerSource interface","IMFSequencerSource interface [Media Foundation]","AppendTopology method","IMFSequencerSource.AppendTopology","IMFSequencerSource::AppendTopology","mf.imfsequencersource_appendtopology","mfidl/IMFSequencerSource::AppendTopology"]
old-location: mf\imfsequencersource_appendtopology.htm
tech.root: mf
ms.assetid: 4ff20d56-6095-495d-89ee-9086c61da8ac
ms.date: 12/05/2018
ms.keywords: 4ff20d56-6095-495d-89ee-9086c61da8ac, AppendTopology, AppendTopology method [Media Foundation], AppendTopology method [Media Foundation],IMFSequencerSource interface, IMFSequencerSource interface [Media Foundation],AppendTopology method, IMFSequencerSource.AppendTopology, IMFSequencerSource::AppendTopology, mf.imfsequencersource_appendtopology, mfidl/IMFSequencerSource::AppendTopology
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSequencerSource::AppendTopology
 - mfidl/IMFSequencerSource::AppendTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSequencerSource.AppendTopology
---

# IMFSequencerSource::AppendTopology


## -description

Adds a topology to the end of the queue.

## -parameters

### -param pTopology [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the topology. This pointer cannot be <b>NULL</b>. If an application passes <b>NULL</b>, the call fails with an E_INVALIDARG error code.

### -param dwFlags [in]

A combination of flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags">MFSequencerTopologyFlags</a> enumeration.

### -param pdwId [out]

Receives the sequencer element identifier for this topology.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The source topology node is missing one of the following attributes:

<ul>
<li>

<a href="/windows/desktop/medfound/mf-toponode-stream-descriptor-attribute">MF_TOPONODE_STREAM_DESCRIPTOR</a>


</li>
<li>

<a href="/windows/desktop/medfound/mf-toponode-presentation-descriptor-attribute">MF_TOPONODE_PRESENTATION_DESCRIPTOR</a>


</li>
<li>

<a href="/windows/desktop/medfound/mf-toponode-source-attribute">MF_TOPONODE_SOURCE</a>


</li>
</ul>
</td>
</tr>
</table>

## -remarks

The sequencer plays topologies in the order they are queued. You can queue as many topologies as you want to preroll.

The application must indicate to the sequencer when it has queued the last topology on the Media Session. To specify the last topology, set the SequencerTopologyFlags_Last flag in the <i>dwFlags</i> parameter when you append the topology. The sequencer uses this information to end playback with the pipeline. Otherwise, the sequencer waits indefinitely for a new topology to be queued.

## -see-also

<a href="/windows/desktop/medfound/about-the-sequencer-source">About the Sequencer Source</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource">IMFSequencerSource</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode">MFCreateTopologyNode</a>