---
UID: NN:vidcap.ISelector
title: ISelector (vidcap.h)
description: The ISelector interface is used to select source nodes in a stream class driver.
helpviewer_keywords: ["ISelector","ISelector interface [DirectShow]","ISelector interface [DirectShow]","described","ISelectorInterface","dshow.iselector","vidcap/ISelector"]
old-location: dshow\iselector.htm
tech.root: dshow
ms.assetid: bd6e028c-ed6d-4dad-a276-c59ba9d88e87
ms.date: 12/05/2018
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
<li>Use the <a href="/windows/previous-versions/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo</a> interface to enumerate the nodes and discover the node types, identifiers, and names.</li>
<li>Call <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> to create the selector node, passing in the node identifier and the interface identifier IID_ISelector. The method returns an <code>ISelector</code> interface pointer.</li>
<li>Use the <code>ISelector</code> interface to select the source node.</li>
</ol>
The <code>ISelector</code> interface is available if the selector node supports the PROPSETID_VIDCAP_SELECTOR property set. For more information, see the Windows DDK documentation.
