---
UID: NN:vidcap.ISelector
title: ISelector (vidcap.h)
description: The ISelector interface is used to select source nodes in a stream class driver.
helpviewer_keywords: ["ISelector","ISelector interface [DirectShow]","ISelector interface [DirectShow]","described","ISelectorInterface","dshow.iselector","vidcap/ISelector"]
old-location: dshow\iselector.htm
tech.root: dshow
ms.assetid: bd6e028c-ed6d-4dad-a276-c59ba9d88e87
ms.date: 4/26/2023
ms.keywords: ISelector, ISelector interface [DirectShow], ISelector interface [DirectShow],described, ISelectorInterface, dshow.iselector, vidcap/ISelector
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISelector
 - vidcap/ISelector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - ISelector
---

# ISelector interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ISelector</code> interface is used to select source nodes in a stream class driver. Applications can use this interface to select which input is active on the device. For example, if a USB video capture device has a camera and a tape transport, these inputs could be represented as source nodes.

## -inheritance

The <b>ISelector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISelector</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

A kernel-streaming (KS) filter contains one or more <i>nodes</i>. Each node encapsulates a processing task that is applied to the stream. In the following diagram, nodes 1 and 2 are <i>source</i> nodes and node 3 is a <i>selector</i> node.

<img alt="KsProxy nodes" border="0" src="./images/ksproxynodes.png"/>

The source nodes represent input streams—for example, a camera or a tape transport. The selector node controls which stream is sent to the filter's output pin. To switch between inputs, an application would do the following:

<ol>
<li>Use the <a href="/previous-versions/ms785846(v=vs.85)">IKsTopologyInfo</a> interface to enumerate the nodes and discover the node types, identifiers, and names.</li>
<li>Call <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> to create the selector node, passing in the node identifier and the interface identifier IID_ISelector. The method returns an <code>ISelector</code> interface pointer.</li>
<li>Use the <code>ISelector</code> interface to select the source node.</li>
</ol>
The <code>ISelector</code> interface is available if the selector node supports the PROPSETID_VIDCAP_SELECTOR property set. For more information, see the Windows DDK documentation.
