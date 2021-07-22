---
UID: NF:mfidl.IMFTopology.GetSourceNodeCollection
title: IMFTopology::GetSourceNodeCollection (mfidl.h)
description: Gets the source nodes in the topology.
helpviewer_keywords: ["9da7d4cd-ad83-4d64-9773-699f39625056","GetSourceNodeCollection","GetSourceNodeCollection method [Media Foundation]","GetSourceNodeCollection method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","GetSourceNodeCollection method","IMFTopology.GetSourceNodeCollection","IMFTopology::GetSourceNodeCollection","mf.imftopology_getsourcenodecollection","mfidl/IMFTopology::GetSourceNodeCollection"]
old-location: mf\imftopology_getsourcenodecollection.htm
tech.root: mf
ms.assetid: 9da7d4cd-ad83-4d64-9773-699f39625056
ms.date: 12/05/2018
ms.keywords: 9da7d4cd-ad83-4d64-9773-699f39625056, GetSourceNodeCollection, GetSourceNodeCollection method [Media Foundation], GetSourceNodeCollection method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetSourceNodeCollection method, IMFTopology.GetSourceNodeCollection, IMFTopology::GetSourceNodeCollection, mf.imftopology_getsourcenodecollection, mfidl/IMFTopology::GetSourceNodeCollection
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
 - IMFTopology::GetSourceNodeCollection
 - mfidl/IMFTopology::GetSourceNodeCollection
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
 - IMFTopology.GetSourceNodeCollection
---

# IMFTopology::GetSourceNodeCollection


## -description

Gets the source nodes in the topology.

## -parameters

### -param ppCollection [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a> interface. The caller must release the pointer. The collection contains <b>IUnknown</b> pointers to all of the source nodes in the topology. Each pointer can be queried for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. The collection might be empty.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getnodetype">IMFTopologyNode::GetNodeType</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>