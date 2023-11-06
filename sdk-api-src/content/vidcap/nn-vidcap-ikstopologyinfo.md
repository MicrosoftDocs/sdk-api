---
UID: NN:vidcap.IKsTopologyInfo
title: IKsTopologyInfo (vidcap.h)
description: The IKsTopologyInfo interface enumerates the nodes in a stream class driver. The KsProxy filter exposes this interface. Applications can use this interface to examine the internal topology of a kernel-mode filter.
helpviewer_keywords: ["IKsTopologyInfo","IKsTopologyInfo interface [DirectShow]","IKsTopologyInfo interface [DirectShow]","described","IKsTopologyInfoInterface","dshow.ikstopologyinfo","vidcap/IKsTopologyInfo"]
old-location: dshow\ikstopologyinfo.htm
tech.root: dshow
ms.assetid: 641a10fe-8e8c-4225-b05e-b09dfb5f2fee
ms.date: 4/26/2023
ms.keywords: IKsTopologyInfo, IKsTopologyInfo interface [DirectShow], IKsTopologyInfo interface [DirectShow],described, IKsTopologyInfoInterface, dshow.ikstopologyinfo, vidcap/IKsTopologyInfo
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
 - IKsTopologyInfo
 - vidcap/IKsTopologyInfo
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
 - IKsTopologyInfo
---

# IKsTopologyInfo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IKsTopologyInfo</code> interface enumerates the nodes in a stream class driver. The KsProxy filter exposes this interface. Applications can use this interface to examine the internal topology of a kernel-mode filter.

## -inheritance

The <b>IKsTopologyInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsTopologyInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

In the Windows Driver Model, a kernel-streaming (KS) filter contains one or more <i>nodes</i>. Each node encapsulates a processing task that is applied to the stream. Nodes have inputs and outputs, which connect either to other nodes in the filter, or else to the filter's pins. In this way, the nodes resemble a miniature "filter graph" inside the filter, which may contain several possible data paths. Applications can use the <code>IKsTopologyInfo</code> interface to get information about the nodes and the node connections.

<img alt="KsFilter nodes" border="0" src="./images/ksproxynodes.png"/>

Some devices also support the <a href="/windows/desktop/api/vidcap/nn-vidcap-iselector">ISelector</a> interface for selecting input nodes. For example, if a video capture device has a camera and a tape transport, these could be represented as two nodes (see the previous diagram).

Include Vidcap.h from the Windows SDK or from the DirectX 9.0 SDK Update (Summer 2004) or later.

## -see-also

<a href="/windows/desktop/DirectShow/working-with-usb-dv-video-devices">Working with USB DV Video Devices</a>
