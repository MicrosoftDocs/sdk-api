---
UID: NN:netlistmgr.IEnumNetworks
title: IEnumNetworks (netlistmgr.h)
description: The IEnumNetworks interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the INetworkListManager interface.
helpviewer_keywords: ["IEnumNetworks","IEnumNetworks interface [Network Awareness]","IEnumNetworks interface [Network Awareness]","described","netlistmgr/IEnumNetworks","nla.ienumnetworks"]
old-location: nla\ienumnetworks.htm
tech.root: nla
ms.assetid: ce2b65e5-89fe-48c9-aa00-373406891d02
ms.date: 12/05/2018
ms.keywords: IEnumNetworks, IEnumNetworks interface [Network Awareness], IEnumNetworks interface [Network Awareness],described, netlistmgr/IEnumNetworks, nla.ienumnetworks
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
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
 - IEnumNetworks
 - netlistmgr/IEnumNetworks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - IEnumNetworks
---

# IEnumNetworks interface


## -description

The <b>IEnumNetworks</b> interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a> interface.

## -inheritance

The <b>IEnumNetworks</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetworks</b> also has these types of members:

## -remarks

The list of connected or disconnected networks is cached by <b>IEnumNetworks</b> when it is instantiated. This list is not updated when the connectivity state of a network changes. The <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> interface is recommended for retrieving the current  connectivity state of a network.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>
