---
UID: NN:mfidl.IMFMediaSourceTopologyProvider
title: IMFMediaSourceTopologyProvider (mfidl.h)
description: Enables an application to get a topology from the sequencer source.
helpviewer_keywords: ["7c08fb54-6a78-4b6d-aae7-4b3a823eb880","IMFMediaSourceTopologyProvider","IMFMediaSourceTopologyProvider interface [Media Foundation]","IMFMediaSourceTopologyProvider interface [Media Foundation]","described","mf.imfmediasourcetopologyprovider","mfidl/IMFMediaSourceTopologyProvider"]
old-location: mf\imfmediasourcetopologyprovider.htm
tech.root: mf
ms.assetid: 7c08fb54-6a78-4b6d-aae7-4b3a823eb880
ms.date: 12/05/2018
ms.keywords: 7c08fb54-6a78-4b6d-aae7-4b3a823eb880, IMFMediaSourceTopologyProvider, IMFMediaSourceTopologyProvider interface [Media Foundation], IMFMediaSourceTopologyProvider interface [Media Foundation],described, mf.imfmediasourcetopologyprovider, mfidl/IMFMediaSourceTopologyProvider
f1_keywords:
- mfidl/IMFMediaSourceTopologyProvider
dev_langs:
- c++
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
- IMFMediaSourceTopologyProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSourceTopologyProvider interface


## -description


Enables an application to get a topology from the sequencer source. This interface is exposed by the sequencer source object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceTopologyProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSourceTopologyProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceTopologyProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology">GetMediaSourceTopology</a>
</td>
<td align="left" width="63%">
Returns a topology for a media source that builds an internal topology.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sequencer-source">Sequencer Source</a>
 

 

