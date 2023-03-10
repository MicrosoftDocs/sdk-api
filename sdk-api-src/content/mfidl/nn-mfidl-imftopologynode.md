---
UID: NN:mfidl.IMFTopologyNode
title: IMFTopologyNode (mfidl.h)
description: Represents a node in a topology.
helpviewer_keywords: ["01d7eb7c-a3d3-4924-a8ec-a67e9dc17424","IMFTopologyNode","IMFTopologyNode interface [Media Foundation]","IMFTopologyNode interface [Media Foundation]","described","mf.imftopologynode","mfidl/IMFTopologyNode"]
old-location: mf\imftopologynode.htm
tech.root: mf
ms.assetid: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424
ms.date: 12/05/2018
ms.keywords: 01d7eb7c-a3d3-4924-a8ec-a67e9dc17424, IMFTopologyNode, IMFTopologyNode interface [Media Foundation], IMFTopologyNode interface [Media Foundation],described, mf.imftopologynode, mfidl/IMFTopologyNode
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
 - IMFTopologyNode
 - mfidl/IMFTopologyNode
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
 - IMFTopologyNode
---

# IMFTopologyNode interface


## -description

Represents a node in a topology. The following node types are supported:
<ul>
<li>Output node. Represents a media sink.
            </li>
<li>Source node. Represents a media stream.
            </li>
<li>Transform node. Represents a Media Foundation Transform (MFT).
            </li>
<li>Tee node. Delivers a media stream to two or more nodes.
            </li>
</ul>To create a new node, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode">MFCreateTopologyNode</a> function.

## -inheritance

The <b>IMFTopologyNode</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFTopologyNode</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>



<a href="/windows/desktop/medfound/topology-node-attributes">Topology Node Attributes</a>
