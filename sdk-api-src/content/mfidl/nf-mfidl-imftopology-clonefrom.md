---
UID: NF:mfidl.IMFTopology.CloneFrom
title: IMFTopology::CloneFrom (mfidl.h)
description: Converts this topology into a copy of another topology.
helpviewer_keywords: ["CloneFrom","CloneFrom method [Media Foundation]","CloneFrom method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","CloneFrom method","IMFTopology.CloneFrom","IMFTopology::CloneFrom","b455aa57-9785-4741-bc3b-1f99cbf4e3d9","mf.imftopology_clonefrom","mfidl/IMFTopology::CloneFrom"]
old-location: mf\imftopology_clonefrom.htm
tech.root: mf
ms.assetid: b455aa57-9785-4741-bc3b-1f99cbf4e3d9
ms.date: 12/05/2018
ms.keywords: CloneFrom, CloneFrom method [Media Foundation], CloneFrom method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],CloneFrom method, IMFTopology.CloneFrom, IMFTopology::CloneFrom, b455aa57-9785-4741-bc3b-1f99cbf4e3d9, mf.imftopology_clonefrom, mfidl/IMFTopology::CloneFrom
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
 - IMFTopology::CloneFrom
 - mfidl/IMFTopology::CloneFrom
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
 - IMFTopology.CloneFrom
---

# IMFTopology::CloneFrom


## -description

Converts this topology into a copy of another topology.

## -parameters

### -param pTopology [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the topology to clone.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does the following:

<ul>
<li>Removes all of the nodes from this topology.
          </li>
<li>Clones the nodes from <i>pTopology</i> and adds them to this topology. The cloned nodes have the same node identifiers as the nodes from <i>pTopology</i>.
          </li>
<li>Connects the cloned nodes to match the connections in <i>pTopology</i>.
          </li>
<li>Copies the attributes from <i>pTopology</i> to this topology.
          </li>
<li>Copies the topology identifier from <i>pTopology</i> to this topology.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>