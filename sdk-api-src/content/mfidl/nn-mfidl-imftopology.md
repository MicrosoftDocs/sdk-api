---
UID: NN:mfidl.IMFTopology
title: IMFTopology (mfidl.h)
description: Represents a topology. A topology describes a collection of media sources, sinks, and transforms that are connected in a certain order.
helpviewer_keywords: ["IMFTopology","IMFTopology interface [Media Foundation]","IMFTopology interface [Media Foundation]","described","f293e9ee-9bd2-4b3e-a4ff-53457ee910f6","mf.imftopology","mfidl/IMFTopology"]
old-location: mf\imftopology.htm
tech.root: mf
ms.assetid: f293e9ee-9bd2-4b3e-a4ff-53457ee910f6
ms.date: 12/05/2018
ms.keywords: IMFTopology, IMFTopology interface [Media Foundation], IMFTopology interface [Media Foundation],described, f293e9ee-9bd2-4b3e-a4ff-53457ee910f6, mf.imftopology, mfidl/IMFTopology
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
 - IMFTopology
 - mfidl/IMFTopology
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
 - IMFTopology
---

# IMFTopology interface


## -description

Represents a topology. A <i>topology</i> describes a collection of media sources, sinks, and transforms that are connected in a certain order. These objects are represented within the topology by <i>topology nodes</i>, which expose the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. A topology describes the path of multimedia data through these nodes.

To create a topology, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology">MFCreateTopology</a>.

## -inheritance

The <b>IMFTopology</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFTopology</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>



<a href="/windows/desktop/medfound/topology-attributes">Topology Attributes</a>
